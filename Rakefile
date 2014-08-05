CC = "gcc"

task :default => "hello"

file "hello" => ["hello.o", "world.o"] do |t|
  sh "#{CC} -o #{t.name} #{t.prerequisites.join(' ')}"
end

rule '.o' => '.c' do |t|
  sh "#{CC} -c #{t.source}"
end
