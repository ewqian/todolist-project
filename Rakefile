require "rake/testtask"
require "find"
require "bundler/gem_tasks"

desc 'Run tests'
task :default => :test

desc 'Say hello'
task :hello do
  puts "hello everybody!"
end

#desc 'Run tests'
#task :test do
#  sh 'ruby ./test/todolist-project-test.rb'
#end

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*-test.rb']
end

desc "List every regular file"
task :list do
  Find.find('.') do |p|
    next if p.include?('/.')
    puts p if File.file?(p)
  end
end