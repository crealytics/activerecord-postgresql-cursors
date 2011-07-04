
# -*- ruby -*-

require 'rubygems'
require 'rubygems/package_task'
require 'rake/testtask'
require 'rdoc/task'

$:.push 'lib'

version = File.read('VERSION') rescue ''

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "activerecord-postgresql-cursors"
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

desc 'Test PostgreSQL extensions'
Rake::TestTask.new(:test) do |t|
  t.pattern = 'test/**/*_test.rb'
  t.verbose = false
end

desc 'Build docs'
Rake::RDocTask.new do |t|
  require 'rdoc'
  t.title = "ActiveRecord PostgreSQL Cursors #{version}"
  t.main = 'README.rdoc'
  t.rdoc_dir = 'doc'
  t.rdoc_files.include('README.rdoc', 'MIT-LICENSE', 'lib/**/*.rb')
end

