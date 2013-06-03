# Redmine cookbook
This cookbook is designed to deploy the Redmine application.

Currently supported:

* Deploy the redmine app from the source
* Install and Manage MySQL by the opscode official recipe
* Install and Manage nginx with Unicorn by the opscode official recipe

Roadmap:

* Support log rotate for Rails, Unicorn logs
* Use node attributes instead of hard coding
* Support USR2 restart process
* Support installing ruby

# Requirements
Chef version 0.10.10+

## Platform

* CentOS

Tested on:

* CentOS 6.4

## Cookbooks

* git
* mysql
* database
* unicorn

## Gemfile.lock
Your redmine app must have `Gemfile.lock` to success `$ bundle install`.

# Usage
TODO

# Attributes
See the `attributes/default.rb` for default values.

* `node["redmine"]["user"]`
* `node["redmine"]["deploy_to"]` - The redmine application's deploy root path
* `node["redmine"]["repo"]` - Repository URL for the redmine application
* `node["redmine"]["revision"]` - The revision to be checked out
* `node["redmine"]["db"]["name"]` - The Database name for redmine

# Recipes
## default
Setup the redmine application.

# Data Bags
This cookbook use the redmine data bag for some password.

# License and Author

Author:: Seigo Uchida (<spesnova@gmail.com>)

Copyright:: 2013 Seigo Uchida (<spesnova@gmail.com>)

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

```
http://www.apache.org/licenses/LICENSE-2.0
```

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.