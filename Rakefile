
# -*- ruby -*-

require 'rubygems'
require 'rake/gempackagetask'
require 'rake/rdoctask'

$:.push 'lib'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "activerecord-postgresql-cursors"
    gem.version = "0.0.1"
    gem.summary = "Provides some support for PostgreSQL cursors in ActiveRecord."
    gem.description = gem.summary
    gem.email = "code@zoocasa.com"
    gem.homepage = "http://github.com/zoocasa/activerecord-postgresql-cursors"
    gem.authors =    [ "J Smith" ]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

desc 'Build docs'
Rake::RDocTask.new do |t|
  require 'rdoc/rdoc'
  t.main = 'README.rdoc'
  t.rdoc_dir = 'doc'
  t.rdoc_files.include('README.rdoc', 'MIT-LICENSE', 'lib/**/*.rb')
end

