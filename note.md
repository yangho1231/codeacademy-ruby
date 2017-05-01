#Ruby Note

Never use quotation marks with booleans.
In ruby you don't need to declare var as variable just enter variable name.

print is similar to prompt and console.log in javascript
puts is same execpt it puts brake after the statement.

uppercase = .upcase
lowercase = .downcase

# is for the comment

Use =begin and =end for longer comments similar to */ /*

gets = grabs what user has inputed and it creates new line after. Ex) print "What is your name?"
chomp = removes extra line
gets.chomp 

String interpolation
Use #{} to input your variable.
Ex) first_name = "Kevin"
puts "Your name is #{first_name}" = gives "Your name is Kevin"

capitalize = makes first letter cap and rest lower.

You don't put () for if statement in Ruby and you will need to type end to end the statement
Ex) if true 
        print true 
    end

else if = elsif

unless = is not true

.gsub! = global substitution
.gsub!(/s/, "th") = replace string "s" with "th"
#LOOPS
#while
i = 1
while i < 51 do
    print i
    i += 1
end
#until
until loop is backward of while loop.
counter = 1
until counter > 10
  puts counter
  counter = counter + 1
end

#for loop
for loop you can do like
for num in 1...10
  puts num
end
... = exclude last number
.. = include last number

#loop
i = 20
loop do
  i -= 1
  print "#{i}"
  break if i <= 0
end
break ends the loop

#next
you can skip certain parts of loop
Ex)
for i in 1..5
  next if i % 2 == 0
  print i
end

#.each
You can loop through using each
array = [1,2,3,4,5]
|x| = var x

array.each do |x|
  x += 10
  print "#{x}"
end

arra.each { 
    |x| x += 10
    print x
}

#.times
Easy way to loop certain numbers
Ex) 10.times { print "Chunky bacon!" }
prints "Chunky bacon" 10 times

#.split
Takes string and turns it into array.
#Some more loop examples

puts "Text to search through: "
text = gets.chomp
puts "Word to redact: "
redact = gets.chomp

words = text.split(" ")

words.each do |word|
  if word != redact
    print word + " "
  else
    print "REDACTED "
  end
end

#array
demo_array = [100, 200, 300, 400, 500]
To print 3rd element in the array
print  demo_array[2]

#hashes
hashes is like object in javascript
hash literal notation
my_hash = { "name" => "Eric",
  "age" => 26,
  "hungry?" => true
}

puts my_hash["name"]
puts my_hash["age"]
puts my_hash["hungry?"]

Create empty hash
var x = Hash.new
my_hash = Hash.new in javascript obj.my_hash = "something"

Ex)
my_hash = Hash.new
put key in to new hash
my_hash["Santa"] = "big boy"

Or

my_hash = {
    "sant": "good"
}

#Looping through Hash

family.each { |x, y| puts "#{x}: #{y}" }
The first place holder = key and second holder = value
Similar to for(var key in x) as Javascript

family = { "Homer" => "dad",
  "Marge" => "mom",
  "Lisa" => "sister",
  "Maggie" => "sister",
  "Abe" => "grandpa",
  "Santa's Little Helper" => "dog"
}