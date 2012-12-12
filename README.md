# Mongomapper::Paperclip

This gem gets Paperclip playing nicely with MongoMapper.

## Installation

Add this line to your application's Gemfile:

    gem 'mongomapper-paperclip'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install mongomapper-paperclip

## Usage

In any model you want to use paperclip simply:

    class User < ActiveRecord::Base
      include MMPaperclip

      has_mm_attached_file :avatar, :styles => { :medium => "300x300>", :thumb => "100x100>" }
    end

Then use paperclip as usual. 

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## EDIT: 

Forked and updated to fix the following issue:

    DEPRECATION WARNING: The InstanceMethods module inside ActiveSupport::Concern will be no longer included automatically. Please define instance methods directly in MongoMapper::Plugins::EmbeddedCallbacks instead.

Originally patched for Earlydoc health management apps: 

http://www.earlydoc.com
