---
layout: post
title:      "Lightbulb Moments in Rails "
date:       2019-03-30 17:57:38 +0000
permalink:  lightbulb_moments_in_rails
---


After completing the Sinatra section, I was warned that Rails would be quite a bit different.  I  really didn't know what to expect but now the meaning of "abstraction" is much clearer. Initially,  it was hard to accept the concept of Convention over Configuration because the minimalization of code is substantial. As a creative and questioning person I need to know how things work and what happens if they don't.  If I'm not writing the code how do I know what the code does. However, the lessons do a good job of explaining and guiding through the process.

Yet there are some "gotchas" along the way - here are 2 concepts that I had issues with but was finally able to get clarified.

**1. Associations in Rails - has_many, belongs_to, has_many_through**

These declarations set up bindings between models which activate macros.  These macros add methods and functionality which would not be accessible without the association. This makes it easier to form class relationships thereby resulting in less code. It also explains a bit of "magic" that happens when building a complex application.

As an example of Rails efficiency, if we check https://apidock.com/rails/ActiveRecord/Associations/ClassMethods - the  has_many macro actually adds another 61 methods automatically just by association. Pretty cool! 

**2. Rails forms** - (A lot of magic)

I found the best way to understand how the form_for, fields_for and collection_select forms was by using dev tools in the browser to see the conversion to HTML. The documentation on these forms can be very intimidating and confusing. After a lot of research on Google which was not fruitful, I decided to use rails console, binding.pry, and browser inspect to see what the code was doing. Once I saw the conversion I was able to understand how to set the params in the form.

The collection_select seemed to be the biggest confusion. Here is the explanation that seemed to be the best.

**Sample usage (selecting the associated Author for an instance of Post, @post):

collection_select(:post, :author_id, Author.all, :id, :name_with_initial, prompt: true)**

*1. collection_select is a **method** which is called on a collection of objects and returns a selection form . Variations include collection_check_boxes and  collection_radio_buttons *
2. The first  field in the parenthesis is the object which the method is called on. NOTE: If this method is being used in a formbuilder, the object field is eliminated  because it is already declared in the form.
3. The second field in the parenthesis is the associated parameter.
4. The third field is the Class.all which will populate the selection
5. The fourth field is the value used for the selection items
6. The fifth field is the label for the selection items  which will be set as text on the form
7. The sixth field is an optional field - see documentation for various options to be added.

Example of conversion
<%= form_for post do |f| %>
...
<%= f.collection_select :category_ids, Category.all, :id, :name %>
...
<select name="post[category_ids]" id="post_category_ids" value="1"></select>

This is just 2 of the sticky points I ran across. Once I was able to wrap my head around convention versus configuration I realized that I appreciate all the work Rails does. The goal is to allow more time and energy on the creative and innovative side of programming. Once I learn it - that would be a great goal. 

