# ipcat-ruby

A ruby port of the [ipcat](https://github.com/client9/ipcat) library to classify IP addresses from known datacenters

## Installation

With bundler:

    # In Gemfile
    gem 'ipcat'

Or with rubygems:

    gem install ipcat

## Usage

    IPCat.datacenter?(ip_address)

It will return an IPCat::IPRange if ip_address is from a known datacenter; nil otherwise.

For example,

    range = IPCat.datacenter?('8.18.145.0') # => instance of IPCat::IPRange
    range.name # => 'Amazon AWS'

    IPCat.datacenter?('127.0.0.1') # => nil

