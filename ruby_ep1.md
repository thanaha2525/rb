## Ruby Ep:1

> version in note


    ➜ ruby -v
    
    ruby 2.6.3p62 (2019-04-16 revision 67580) [universal.x86_64-darwin19]

> Ruby console

    ➜ irb  #ใช้ในกรณีที่อยู่ root
    ➜ rails c   #ใช้ในกรณีที่อยู่ใน Project

**ใน Ruby มองว่าทุกอย่างคือ object**
ไม่ว่าจะ "" ก็เป็น obj  "     " ก็เป็น obj   

อะไรก็ตามที่ถูกตามด้วย ? จะ Return true || false

    ➜ ep3  git:(master) ✗ rails c
    Running via Spring preloader in process 58321
    Loading development environment (Rails 6.0.3.2)
    2.6.3 :001 > ""
    => ""
    2.6.3 :002 > "".empty?
    => true
    2.6.3 :003 > nil
    => nil
    2.6.3 :004 > nil.class
    => NilClass
    2.6.3 :005 > nil.class.superclass
    => Object
    2.6.3 :006 >
    2.6.3 :006 > 1.class
    => Integer
    2.6.3 :007 > 1.class.superclass
    => Numeric
    2.6.3 :008 > 1.3.class
    => Float
    2.6.3 :009 > 1.3.class.superclass
    => Numeric
    2.6.3 :010 >

> if crouse

    2.6.3 :010 > x = 10
    => 10
    2.6.3 :011 > if x >= 10
    2.6.3 :012?> puts "#{x}"
    2.6.3 :014?> end
    => "10"
    

> if crouse in one line

    2.6.3 :017 > puts "hello #{x}" if x >= 10
    hello 10
    => nil
    2.6.3 :018 >

> unless #if not

    2.6.3 :018 > puts "hello #{x}" unless x >= 10
    => nil
same

    2.6.3 :020 > puts "hello #{x}" if !(x >= 10)
    => nil

> if else 

    2.6.3 :021 > if x >= 10
    2.6.3 :022?> puts "hello #{x}"
    2.6.3 :023?> else
    2.6.3 :024?> puts "no 10"
    2.6.3 :025?> end
    hello 10
    => nil
   
   

> Join string

    2.6.3 :001 > x = "hello"
    => "hello"
    2.6.3 :002 > x += 'world'
    => "helloworld"
    2.6.3 :003 > x
    => "helloworld"

> นำค่าจากตัวแปร เข้า string

    2.6.3 :006 > "#{x} + #{y} = #{x+y}"
    => "10 + 20 = 30"

> Print to Console ใช้ puts โดยการ puts จะขึ้นบรรทัดใหม่เท่านั้น

    2.6.3 :007 > puts "#{x} + #{y} = #{x+y}"
    10 + 20 = 30
    => nil
    2.6.3 :008 >  puts "#{x} + #{y} = #{x+y}"
    10 + 20 = 30
    => nil
    2.6.3 :009 >  puts "#{x} + #{y} = #{x+y}"
    10 + 20 = 30
    => nil
    2.6.3 :010 >

> วิธี join code ใช้ ;

    2.6.3 :010 >  puts "#{x} + #{y} = #{x+y}";puts "#{x} + #{y} = #{x+y}";puts "#{x} + #{y} = #{x+y}"
    10 + 20 = 30
    10 + 20 = 30
    10 + 20 = 30

> คำสั่ง print จะอยู่บรรทัดเดียวกัน

    2.6.3 :012 > print "#{x} + #{y} = #{x+y}";print "#{x} + #{y} = #{x+y}";print"#{x} + #{y} = #{x+y}"
    10 + 20 = 3010 + 20 = 3010 + 20 = 30 => nil

> String 

' '  จะมองว่าเป็นทีละ charecter 
" "  จะมองว่า \ เป็น charecter ไปด้วย

    2.6.3 :015 > x = '\n'
    => "\\n"
    2.6.3 :016 > x = "\n"
    => "\n"
    2.6.3 :017 >

    2.6.3 :017 > phase = "asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf\nsdjkljklafakldieada\naldjkfaeidjfa"
    => "asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf\nsdjkljklafakldieada\naldjkfaeidjfa"
    2.6.3 :018 > puts phase
    asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf
    sdjkljklafakldieada
	aldjkfaeidjfa
	=> nil
	2.6.3 :019 > print phase
	asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf
	sdjkljklafakldieada
	aldjkfaeidjfa => nil
	2.6.3 :020 > phase = 'asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf\nsdjkljklafakldieada\naldjkfaeidjfa'
	=> "asdfjsjklafjklasdfjklasjklasdfjkl;sadfjkasdf\\nsdjkljklafakldieada\\naldjkfaeidjfa"
	2.6.3 :021 >
