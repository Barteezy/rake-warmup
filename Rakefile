desc "Print a nice greeting"
task :greet do
  puts "Hello there"
end

desc "Prints your favorite food is"
task :print_favorite_food do
  ENV["FAVORITE_FOOD"] = "Pizza"
  puts "Favorite Food is: #{ENV["FAVORITE_FOOD"]}"
end


task :first do
  puts "First!"
end

task :second => :first do
  puts "Second!"
end

task :wake_up do
  puts "I'm awake!"
end

task :gets_dressed => :wake_up do
  puts "I'm dressed"
end

# - Write a rake task called `ready_for_class`, that depends on tasks called `wake_up`,
#                                                                            `eat_breakfast`, and `brush_teeth`.

task :brush_teeth => :eat_breakfast do
  puts "brush brush brush"
end



task :eat_breakfast => :wake_up do
  puts "I'm eating"
end


task :ready_for_class => :brush_teeth  do
  puts "I'm ready for class"
end

namespace :greeting do
  desc "Say hello"
  task :hello do
    puts "Hello there"
  end

  desc "Say howdy"
  task :howdy do
    puts "Howdy partner"
  end
end

task :default => [:wake_up]