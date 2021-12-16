namespace :greeting do
  desc "outputs hello to terminal"
  task :hello do
    puts "hello from Rake!"
  end
  desc "initaites final warning"
  task :warning do
    puts "You have been warned"
  end
end
namespace :db do
  desc "migrate"
  task migrate: :environment do
    Student.create_table
  end
  desc "seed"
  task seed: :environment do
    require_relative "./db/seeds"
  end
end
task :environment do
  require_relative "./config/environment"
end
desc "console activate"
task console: :environment do
  Pry.start
end