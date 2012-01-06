# -*- coding: utf-8 -*-

require "rubygems"
require "bundler"
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end

require "rake"
require "jeweler"
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "pupil"
  gem.homepage = "http://github.com/oame/pupil"
  gem.license = "MIT"
  gem.summary = %Q{The "Lazy" Twitter API Library for Ruby 1.9.x}
  gem.description = %Q{The "Lazy" Twitter API Library for Ruby 1.9.x. Easy to use.}
  gem.email = "oame@oameya.com"
  gem.authors = ["Oame"]
  gem.required_ruby_version = '~>1.9.0'
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require "rspec/core"
require "rspec/core/rake_task"
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList["spec/**/*_spec.rb"]
end

RSpec::Core::RakeTask.new(:rcov) do |spec|
  spec.pattern = "spec/**/*_spec.rb"
  spec.rcov = true
end

task :default => :spec

require "yard"
YARD::Rake::YardocTask.new
