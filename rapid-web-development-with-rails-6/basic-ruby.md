---
# theme: gaia
class:
  - lead
  # - invert
header: ''
footer: '<img style="width: 200px; " src="studiplex-logo-beta.svg">'
style: |
  section.medium span {
    font-size: 16px;
  }
  .center {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 50%;
  }
---

## Lets greet the world first
```rb
# $ touch main.rb
# $ nano main.rb

puts 'Hello World'

# exit
# ruby main.rb
# => 'Hello World'

```

----


### Did you know about, Pareto's Principle
<img style="width: 270px" src="https://images-eu.ssl-images-amazon.com/images/I/41yXBqTJSAL.jpg" class="center">

** IMHO it can be applied in Software Engineering field too

---

# ~~Java~~ Ruby everything is an object.

---

#### ~~Java~~ Ruby everything is an object - Basic Types I.

<!-- _class: medium -->
```rb
$ irb

> one = 1
=> Integer
> one.positive?
=> true

> nil.class
=> NilClass
> nil.nil?
=> nil.nil?

> "awesome".upcase
=> "AWESOME"

> :awesome.class
=> Symbol

```

---

#### ~~Java~~ Ruby everything is an object - Basic Types II.

```rb
> true.class
=> TrueClass
> false.class
=> FalseClass

> list = Array.new(1,2,3)
> list == [1,2,3]
=> true
> list.size
=> 3

> hash = {'key': 'value', :another_key => 'another_value', other: 'value'}
> hash.class
=> Hash

```

----

## Array, the polymorphic chain

<!-- _class: medium -->

```
chain = [1, 2, :hello, {foo: 'bar'}]
puts chain[0]
# => 1
puts chain[2]
# => :hello
puts chain[3][:foo]
# => 'bar'

# it a also has methods .first, .last,

# slicing
chain[1,2]
# => [2, :hello]

# mutating
chain << 666
chain.pop

```

----

## Hash, the key value association

<!-- _class: medium -->

```
example = { link: :me, to: { 'another' => 'dimension' } }

# get the dimension
example[:to]['another']

# add new key
example[:new] = 'oy oy oy'

```

---

## Function, Conditional, and Loop

```rb
def player_classification(players)
  players.each do |player|
    if player[:skill] < 3
      puts "n00B Player #{payler[:name]}"
    elsif players[:skill] < 8
      puts "Moderate Player #{payler[:name]}"
    else
      puts "Dope Player #{payler[:name]}"
    end
  end
end

players = [{name: 'sindri', skill: 2}, {name: 'atreus', skill: 5}, {name: 'kratos', skill: 10}]

# call the method
player_classification(players)
# player_classification players
# sum 1, 2, 3

# WOW, without parentheses???
```

---

## Ruby Blocks

<!-- _class: medium -->
```
def multiplier(x, y)
  value = x * y

  # for now, let's just assume this `yield` functionality as a callback
  yield value
end

multiplier(6, 3) { |value| puts "the result is #{value}" }

# or

multiplier(6,3) do |value|
  puts "the result is #{value}"
  puts "do another thing with result #{value}"
end

```
** reference: https://mixandgo.com/learn/mastering-ruby-blocks-in-less-than-5-minutes

---

# 🎉 Congrats!, now you know basic ruby syntax and data structures

---

# Any question??
