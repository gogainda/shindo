require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.add_dependency('annals')
    gem.name = "shindo"
    gem.summary = %Q{ruby testing}
    gem.description = %Q{Simple depth first ruby testing}
    gem.email = "me@geemus.com"
    gem.homepage = "http://github.com/geemus/shindo"
    gem.authors = ["geemus (Wesley Beary)"]
    gem.rubyforge_project = "shindo"
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require File.join(File.dirname(__FILE__), 'lib', 'shindo', 'rake')
Shindo::Rake.new

# begin
#   require 'rcov/rcovtask'
#   Rcov::RcovTask.new do |test|
#     test.libs << 'tests'
#     test.pattern = 'tests/**/*_tests.rb'
#     test.verbose = true
#   end
# rescue LoadError
#   task :rcov do
#     abort "RCov is not available. In order to run rcov, you must: sudo gem install spicycode-rcov"
#   end
# end

task :tests => :check_dependencies

task :default => :tests

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  if File.exist?('VERSION')
    version = File.read('VERSION')
  else
    version = ""
  end

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "shindo #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
