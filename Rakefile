namespace :greeting do

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello to the terminal in spanish'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'Make changes to DB'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'Seeds the db with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :environment do
  require_relative './config/environment'
end

desc 'Starts an IRB environment with loaded files'
task :console => :environment do
  Pry.start
end