# Edited State Example | The Ultimate PaperTrail Guide

This project is an example within _The Ultimate PaperTrail Guide_. It is a simple Slack-like application that uses PaperTrail to track message versions and shows when a message has been edited.

![PaperTrail Edited State Example Screenshot](./docs/messages-screenshot.png)

## Setup

To run the demo app, clone it:

    git clone https://github.com/changebase-io/paper-trail-edited-state-example.git
    cd paper-trail-edited-state-example

Install dependencies:

    bundle install

Seed the database:

    bundle exec rails db:setup

And run the development server:

    ./bin/rails

Now if you visit localhost:3000, sign in with the following credentials:

    email:      admin@example.com
    password:   password

## Styling

These projects use [TailwindCSS](https://tailwindcss.com/) to make styling pages a breeze. Note the following when working with Tailwind:

- The config file is `tailwind.config.js`, as in any project with Tailwind.
- There is a single stylesheet for Tailwind at `app/assets/stylesheets/application.tailwind.css`. All custom styling should be added to this file, though ideally this is kept to a minimum.
- You **must use `./bin/rails` to run the development server.** If using `bundle exec rails server`, Tailwind changes will not be processed and you won't see all the styling you expect.

## Forms

[Simple Form](https://github.com/heartcombo/simple_form) is being used to help in quickly spinning up new forms.

_Most_ of the styles for forms are set in the initializer — `config/initializers/simple_form.rb`. When making changes to this file, you need to restart your Rails server to see the changes take effect.
