require 'bundler/setup'
require 'bundler/gem_tasks'
require 'appraisal'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec)

desc "Default: run the unit tests."
task :default => [:all]

# FIXME git dependencies are not updated in rails gemfiles
desc 'Test the plugin under all supported Rails versions.'
task :all => ["appraisal:install"] do |t|
  exec('rake appraisal spec')
end
