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

## SSL for Rails
# Force all access to the app over SSL, use Strict-Transport-Security,
# and use secure cookies.
config.force_ssl = true

* Heroku uses a pure-Ruby webserver called WEBrick, which is easy to set up and run but isn’t good at handling
significant traffic.

# Replace config/puma.rb default with the following:
* workers Integer(ENV['WEB_CONCURRENCY'] || 2)
threads_count = Integer(ENV['RAILS_MAX_THREADS'] || 5)
threads threads_count, threads_count

preload_app!

rackup      DefaultRackup
port        ENV['PORT']     || 3000
environment ENV['RACK_ENV'] || 'development'

on_worker_boot do
  # Worker specific setup for Rails 4.1+
  # See: https://devcenter.heroku.com/articles/
  # deploying-rails-applications-with-the-puma-web-server#on-worker-boot
  ActiveRecord::Base.establish_connection
end
