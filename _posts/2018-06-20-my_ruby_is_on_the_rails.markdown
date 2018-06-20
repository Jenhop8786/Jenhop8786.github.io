---
layout: post
title:      "My Ruby is on the Rails"
date:       2018-06-20 23:37:43 +0000
permalink:  my_ruby_is_on_the_rails
---


I love making the titles of my posts subtly reflect the challenges I face when it comes to this program OR when my project is well on it's way like this one for instance. 

Anyways..YAY!! 
I reached my 3rd project, and I had to implement the Ruby on Rails Framework. When I read other students' posts describing their experience with this particular project and how it was the most difficult so far, I didn't even question it.  It just looked intimidating. 

I mean, at a glance, you see majority of the requirements are VERY similiar to the Sinatra Project so immediatly you think it can't be that hard. BUT I knew better than that. I knew that it wasn't going to be as easy as it fancied to be. I wasn't buying this "Rails Magic".. Not yet, at least. 
I created an application for coaches to create assignments with specific tasks to complete. This was inspired by my husband who is a basketball coach and dislikes writing and sending individual emails outlining what they need to do during the time they weren't together for practices.

Fast forward to the initial -rails "do this" command line .. .. command? 
 
``` 
rails g migration CreateAssignments
```
press enter and open my migration file. I don't like to add what my column needs in the initial command so I can add that stuff in the file if I think I need to add additional columns. 

```
class CreateAssignments< ActiveRecord::Migration[5.2]
  def change
    create_table :assignments do |t|
      t.string :title
			```
			
I felt good about that part. Avi once said, you always want to start with the lowest generator, so that's what I did and I will agree that, starting with the basic generators you can really get a better understanding of how your application fits and works all together because YOU wrote everything (well almost everything).  I was tempted to use the Resource generator in the beginning  but I wanted to make sure I didn't get lost in the abyss of all the files that would magically appear and knowing me, I would have filled all of them in without rhyme or reason and ended up with a broken application. 

SO I made my migration and I looked at the requirements. 
The first requirement is to have a **has_many** relationship, and we know that goes in the Model (reminding myself) that as much of the logic NEEDS to go into the Model. I created another migration for Tasks and then stubbed out the associated with my Assignments and Tasks. 
```
class Assignment < ApplicationRecord
  has_many :tasks
end
```
That was easy. 

Then we have the requirement to have nested routes. I wasn't too confident with this one because you still want to remain RESTful as well. 
Even after the millionth re-watch of Avi's explaination, I wasn't that confident BUT I had a good idea of what I needed to do.  When you start working with routes it can get messy really quick. And I didn't even need to learn that the hard way. I just ```raked routes``` in my Terminal

aaaannd I quit for the day. 

When I returned to this window of foreign languages I focused in on the Routes part and mapped out how things were supposed to connect (in my head) then I moved some things around and typed some words in the routes.rb file and prayed for a miracle. 

I returned to my view & controller files, typed a few things in there and hoping that what I was doing would return the outcome I wanted and *needed* so when I went to my browser and hit refresh, I inspected the URL and it was exactly how it should have been. 

```
blah/:2/bleh/ :2 
```
Those aren't my real route names, but you get the picture. 

Feeling accomplished at this point, I wanted to be done before all this luck ran out. 
So, now that I have that requirement out of the way I still needed the Signup/Thirdparty Signup requirement. 
 ***Eeeshh and sheeesh... ***
 
Who would I use? I made it a more challenging decision than it needed to be, like I do everything else. I was stuck between using FaceBook or Github, in the end I winded up implenting Facebook to use as another option to sign into my application and also used Devise as my authenticator. Devise was another intimidating aspect but after digesting as many resources as I could, I ended up being really comfortable with implementing it in my application. 

Overall, this project was challenging, it made me feel every emotion in human existance. I knew becoming a Web Developer through this type of avenue (self-paced and sort of self-taught) was going to be difficult and time consuming but I never imagined it being as mentally tasking (in a good way of course) as it has been. And after the amount of Rails Guides I had consumed I felt like I better be a Senior developer by the time I finish with this bootcamp. 

Just kidding... 
a little... 
