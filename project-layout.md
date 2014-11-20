title: Project Layouts
author:
  name: Alex Dunae
  twitter: mrmrbug
  url: https://github.com/alexdunae/nic-igm240
output: project-layout.html
controls: true

--

# Project Layouts

--

### Project Layouts
Your new secret decoder ring

- part 1: reading them
- part 2: creating them

--

### Project layouts

Path names say a lot and can get you into the mind of the people who wrote the code.

- what are the components?
- what does it do?
- how does it do it?
- what seems important?

--

### Project layouts in Ruby

The Ruby community has settled on some conventions

- one object per file
- directories mirror namespaces

So let's start with the 800 lb. gorilla and look at Rails' default structure...

--


### The default structure of a Rails app

Looking at the Rails project structure tells us what Rails considers important.


- `app`
- `config`
- `db`
- `test`

(These are the important paths; there are a few others as well.)

--

### The default structure of a Rails app

#### /app

This must be where your application goes?!

- `app/controllers`
- `app/helpers`
- `app/models`
- `app/views`

--

### The structure of a Rails app

#### /config

- `config/application.rb`
- `config/database.yml`
- `config/environments/development.rb`
- `config/environments/production.rb`
- `config/secrets.yml`

There are a lot of files here. Having configuration separate must be important.

--

### The structure of a Rails app

#### /db

- `db/schema.rb`
- `db/migrations/01_create_blog.rb`

The database is considered separately from the main application.

--

### The structure of a Rails app

#### /test

- `test/controllers`
- `test/helpers`
- `test/models`
- `test/integration`

These match up with what was in the `/app` directory.

<small>* The actual directory names are a little different.</small>

--

### The structure of a Rails app

Those were just the defaults. In Ruby, objects (and therefore files) are cheap. Use them to communicate to future developers (including yourself).

--

### A Rails app meets reality

- **`app/api`**
- `app/controllers`
- **`app/forms`**
- `app/helpers`
- **`app/mailers`**
- `app/models`
- **`app/pdfs`**
- **`app/reporters`**
- **`app/serializers`**
- **`app/services`**
- **`app/values`**
- **`app/workers`**

-- 

# Let's checkout a few projects

--

### `money` gem

- `lib/bank`
	- `single_currency.rb`
	- `variable_exchange.rb`
- `lib/currency.rb`
- `lib/currency`
	- `heuristics.rb`
- `lib/money.rb`
- `lib/money`
	- `arithmetic.rb`
	- `formatting.rb`

--

### `barby` gem

- `lib/barby.rb`
- `lib/barby/barcode.rb`
- `lib/barby/barcode`
	- `code_128.rb`
	- `qr_code.rb`
- `lib/barby/outputter.rb`
- `lib/barby/outputter`
	- `html_outputter.rb`
	- `png_outputter.rb`
	- `svg_outputter.rb`

--

# So... project layout matters, right?

--

### Let's layout a project

...

<small>Maybe a back-up system with objects representing the file system, service objects processing the backups...</small>

--

### A few more Ruby conventions

- `Gemfile` for dependencies
- `Rakefile` for automation
- `README`, `LICENSE`, `CHANGELOG`
- `lib/version.rb`

--

### Project Layouts

Your new secret decoder ring

- the codification of your design decisions
- a clue to future developers: how does this thing work?
- an invitation to collaboration
