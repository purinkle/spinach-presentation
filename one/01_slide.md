!SLIDE
# spinach
## or how to troll the office using BDD

!SLIDE incremental bullets
* spinach
* cucumber
* steak
* the rest

!SLIDE incremental
# write a feature

     @@@ cucumber
     Scenario: Poke Pingham in the ribs
      Given I am stood next to Pingham
      When I jab Pingham hard in the ribs
      Then Pingham winces like a girl

!SLIDE

    @@@ ruby
    class TrollPingham
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

    @@@ ruby
    class TrollPingham
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
# features/support/locations.rb
    @@@ ruby
    class Locations
      include Spinach::DSL

      Given 'I am stood next to Pingham' do
        …
      end

      …
    end
