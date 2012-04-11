# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "peepshow"
  gem.homepage = "http://github.com/awebneck/peepshow"
  gem.license = "MIT"
  gem.summary = %Q{A library for easing the use of SQL views in ActiveRecord}
  gem.description = %Q{Need to create SQL views that you can interact with as ActiveRecord objects? This is your one-stop (actually maintained) shop. Based on some of the excellent work done by Anthony Eden in his rails_sql_views plugin, this bad boy is ready to rock for Rails 3.1+ and will be actively maintained moving forward to keep up with the latest and greatest.}
  gem.email = "jeremy@jeremypholland.com"
  gem.authors = ["Jeremy Holland"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "peepshow #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
