require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the acts_as_favorite plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the acts_as_favorite plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'ActsAsFavorite'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "acts_as_favorite"
    gemspec.summary = "User fovorites for you web application"
    gemspec.description = "This gem provides a simple way to track users favorites within the system using ActiveRecord models"
    gemspec.email = "kossnocorp@gmail.com"
    gemspec.homepage = "http://github.com/kossnocorp/acts_as_favorite"
    gemspec.authors = ["Josh Martin"]
    gemspec.version = "0.1"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end
