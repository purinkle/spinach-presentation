!SLIDE
# spinach
## or how to troll the office using BDD

!SLIDE incremental bullets
* spinach
* cucumber
* steak
* the rest

!SLIDE incremental
features/troll_pingham.feature

     @@@ cucumber
     Feature: Troll Pingham
     In order to get through my working day
     As an On the Beach developer
     I need to constantly troll Pingham

     Scenario: Poke Pingham in the ribs
      Given I am stood next to Pingham
      When I jab Pingham hard in the ribs
      Then Pingham winces like a girl

!SLIDE
features/steps/troll_pingham.rb

    @@@ ruby
    class TrollPingham < Spinach::FeatureSteps
      Given 'I am stood next to Pingham' do
        …
      end

      When 'I jab him hard in the ribs' do
        …
      end

      Then 'Pingham winces like a girl' do
        …
      end
    end

!SLIDE
features/steps/troll_pingham.rb

    @@@ ruby
    class TrollPingham < Spinach::FeatureSteps
      …

      When 'I jab him hard in the ribs' do
        …
      end

      When 'I tape all his stuff to his desk' do
        …
      end

      …

      Then 'Pingham winces like a girl' do
        …
      end

      Then 'Pingham gets in a huff' do
        …
      end

      …
    end

!SLIDE
# urgh!

!SLIDE
# just assertions

!SLIDE incremental bullets
# support files
* locations
* trolls
* whatever

!SLIDE
features/support/locations.rb
    @@@ ruby
    module Locations
      include Spinach::DSL

      Given 'I am stood next to Pingham' do
        …
      end

      …
    end

!SLIDE
features/support/trolls.rb
    @@@ ruby
    module Trolls
      include Spinach::DSL

      When 'I jab him hard in the ribs' do
        …
      end

      When 'I tape all his stuff to his desk' do
        …
      end

      …
    end

!SLIDE
features/steps/troll_pingham.rb

    @@@ ruby
    class TrollPingham < Spinach::FeatureSteps
      include Locations
      include Trolls

      Then 'Pingham winces like a girl' do
        …
      end

      Then 'Pingham gets in a huff' do
        …
      end

      …
    end

!SLIDE
features/steps/troll_matt.rb

    @@@ ruby
    class TrollMatt < Spinach::FeatureSteps
      include Locations
      include Trolls

      Then 'Matt reaches for a clawhammer' do
        …
      end

      …
    end

!SLIDE incremental bullets
# red, green, refactor

!SLIDE incremental bullets
# git

* `features/troll_pingham.feature`
* `feature/2012-12-21-troll-pingham`

!SLIDE
# VCR

!SLIDE
[http://devblog.avdi.org/2011/04/11/screencast-taping-api-interactions-with-vcr/](http://devblog.avdi.org/2011/04/11/screencast-taping-api-interactions-with-vcr/)

!SLIDE
# `using_vcr_cassette`

!SLIDE
    @@@ruby
    using_vcr_cassette('whittle does dallas') do
      …
    end

!SLIDE
# kthxbai!
