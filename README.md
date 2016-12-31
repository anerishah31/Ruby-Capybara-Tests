# Ruby Capybara Tests
[//]: # "[![Travis Status](https://travis-ci.org/saucelabs-sample-test-frameworks/Ruby-RSpec-Selenium.svg?branch=master)](https://travis-ci.org/saucelabs-sample-test-frameworks/Ruby-RSpec-Selenium)"

## Important Disclaimer
This code is provided on an "AS-IS” basis without warranty of any kind, either express or implied, 
including without limitation any implied warranties of condition, uninterrupted use, merchantability, 
fitness for a particular purpose, or non-infringement. 
Your tests and testing environments may require you to modify this project. 
For questions regarding Sauce Labs integration, please see the [Sauce Labs documentation](https://wiki.saucelabs.com/). 
This project is not maintained by Sauce Labs Support.


## Purpose
Use this project as example code if you have an existing Capybara implementation, or if
you have an existing Rails application and the developers who will be creating and 
implementing the new test suite have experience with Capybara.

If you do not have an existing project and would like to use Ruby, 
it is recommended to look at the [Watir Tests Repo](https://github.com/titusfortner/Ruby-Watir-Tests). 

If you already have an existing test suite and are just looking to add Sauce Labs 
functionality to that project, or if you need to run tests on a mobile application,
take a look at the [Ruby Example Tests](http://www.notimplementedyet.com) project.

 
## Technologies used in this project:

#### RSpec
1. [Pass Information to Saucelabs](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/spec/spec_helper.rb#L12-L26)
2. [Execute Tests in Parallel](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/Rakefile#L26)
3. [Integrate with Applitools](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/spec/spec_helper.rb#L28-L32)

### Cucumber
1. [Pass Information to Saucelabs](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/features/support/env.rb#L12-L25)
2. [Execute Tests in Parallel](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/Rakefile#L35)
3. [Integrate with Applitools](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/features/support/env.rb#L27-L31)

### Site Prism
5. [Site Prism Example](https://github.com/titusfortner/Ruby-Capybara-Tests/blob/master/lib/pages/guinea_pig_page.rb)


## Requirements to Run These Examples

1. Global Dependencies
    * [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/)
    * If on Mac install Ruby with [Homebrew](http://brew.sh/)
    ```
    $ brew install ruby
    ```
    * Install [Rake](http://docs.seattlerb.org/rake/)
    ```
    $ gem install rake
    ```
    * Install bundler (Sudo may be necessary)
    ```
    $ gem install bundler
    ```

2. Sauce Credentials
    * In the terminal export your Sauce Labs Credentials as environmental variables:
    ```
    $ export SAUCE_USERNAME=<your Sauce Labs username>
	$ export SAUCE_ACCESS_KEY=<your Sauce Labs access key>
    ```

3. Project Dependencies
	* Install packages (Use sudo if necessary)
	```
	$ bundle install
	```
    * Set Build ID (Optional)
    ```
    $ export BUILD_TAG=sauce_automated_build_name
    ```


## Running Tests

1. Run RSpec specs on Sauce in Parallel:
	```
	$ bundle exec rake test_rspec
	```

2. Run Cucumber Features on Sauce in Parallel:
	```
	$ bundle exec rake test_cucumber
	```

3. Execute Tests on Sauce in Parallel using an environment variable:
	```
	$ TEST_RUNNER=rspec bundle exec rake
	```

View the results on your [Sauce Labs Dashboard](https://saucelabs.com/beta/dashboard/)


### Contributing

This project is open source! 
The maintainers welcome the community to [submit an issue](http://notimplementedyet.com/issues#new) with ideas or bug reports, 
and [making pull requests](http://notimplementedyet.com/pulls#new) with bug fixes and suggested code improvements


## License

This project is available under the terms of the [MIT License](http://opensource.org/licenses/MIT).


## Additional Resources
##### [Sauce Labs Documentation](https://wiki.saucelabs.com/)

##### [Capybara Documentation](https://github.com/teamcapybara/capybara#readme)

##### [SeleniumHQ Documentation](http://www.seleniumhq.org/docs/)

##### [RSpec Documentation](http://rspec.info/documentation/)

##### [Cucumber Documentation](https://cucumber.io/docs/)

##### [Applitools Documentation](https://applitools.com/resources/#Documentation/)

##### [Site Prism Documentation](https://github.com/natritmeyer/site_prism#readme)

##### [Ruby Documentation](http://ruby-doc.org/)

##### [Stack Overflow](http://stackoverflow.com/)
* A great resource to search for issues not explicitly covered by documentation.
