# -*- mode: ruby -*-

# Require the AWS provider plugin
require 'vagrant-aws'

# Create and configure the AWS instance(s)
Vagrant.configure('2') do |config|

  # Use dummy AWS box
  config.vm.box = 'aws-dummy'

  # Specify AWS provider configuration
  config.vm.provider 'aws' do |aws, override|
    # Read AWS authentication information from environment variables
    aws.access_key_id = ENV['AWS_ACCESS_KEY_ID']
    aws.secret_access_key = ENV['AWS_SECRET_ACCESS_KEY']

    # Specify SSH keypair to use
    aws.keypair_name = ENV['AWS_KEYPAIR_ID']

    # Specify region, AMI ID, and security group(s)
    aws.region = 'eu-west-1'
    aws.ami = 'ami-9398d3e0'
    aws.security_groups = ['default']

    # Specify username and private key path
    override.ssh.username = 'ec2-user'
    override.ssh.private_key_path = ENV['AWS_PRIV_KEY_PATH']

    # Instance configuration
    aws.instance_type = 't2.micro'
    aws.tags = {
      'Name' => 'dev-' + ENV['AWS_KEYPAIR_ID'] + '-vagrant-' + ("%04d" % rand(9999))
    }
  end
end
