require "bundler/gem_tasks"
require "rake/testtask"
require 'yard'

namespace :test do
  Rake::TestTask.new(:spec) do |t|
    t.libs << "test"
    t.test_files = FileList['test/spec/*_spec.rb']
  end

  Rake::TestTask.new(:unit) do |t|
    t.libs << "test"
    t.test_files = FileList['test/unit/**/*_test.rb']
  end
end

task :test => ['test:spec', 'test:unit']

task :default => :test

YARD::Rake::YardocTask.new do |t|
  t.options = ['-m', 'markdown']
end
