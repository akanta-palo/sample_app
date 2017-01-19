# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* to destroy generated element: rails destroy  controller StaticPages home help

* generate model: rails generate model User name:string email:string

* migrate data: rails db:migrate

* undo a single db migration: rails db:rollback

* rollback completely: rails db:migrate VERSION=0

* special rails function provide: <% provide(:title, "Home") %>, <%= yield(:title) %>

* rails generate new controller: rails generate controller ControllerName <optional action names>

* attr accessor allows retrieve (get) and assign (set)

* debug(params) if Rails.env.development? to display the debug log

* assert_no_difference will result in no difference of the user.count at the start and the end of test.

* assert_template checks that failed submission will re-render the new action
