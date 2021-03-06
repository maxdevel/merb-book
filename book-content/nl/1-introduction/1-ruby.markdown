# Ruby

* This will become a table of contents (this text will be scraped).
{:toc}

![Ruby](/images/ruby-header.gif){: .no-border}

**Reference website:** [http://ruby-lang.org](http://ruby-lang.org){: .reference}

> Coderen in Ruby maakt me gelukkig omdat het een van de kortste paden is tussen mijn hersenen en een computer. Als ik aan iets denk, kan ik het bondig uitdrukken en meestal ook op een vrij elegante wijze in Ruby zonder de vreemde kronkels die nodig zijn in de meeste andere talen.
> - [Dave Thomas, auteur van "Programming Ruby"](http://pragdave.pragprog.com/){: .quote-author}
{: cite=http://www.infoq.com/interviews/ruby-rails-dave-thomas .lead-quote}

Het zou misdadig zijn te over over het Merb framework te beginnen spreken zonder het eerst te hebben over de echte reden waarom Merb zo flexibel, krachtig, en snel is: **Ruby**.

## Oorsprong ##{: #origin}
![Yukihiro Matsumoto](/images/Yukihiro_Matsumoto.jpg){: .left}
Ruby is een [Open Source](http://en.wikipedia.org/wiki/Open_Source), [dynamische](http://en.wikipedia.org/wiki/Dynamic), [reflectieve](http://en.wikipedia.org/wiki/Reflection_%28computer_science%29), algemeen-doel, [object-georienteerde](http://en.wikipedia.org/wiki/Object-oriented_programming) [programmeertaal](http://en.wikipedia.org/wiki/Programming_language) geschreven midden de jaren 90 door de japanse [software architect](http://en.wikipedia.org/wiki/Software_architect) [Yukihiro "Matz" Matsumoto-san ( まつもとゆきひろ)](http://en.wikipedia.org/wiki/Yukihiro_Matsumoto).

Ruby focust op eenvoud en productiviteit. Ruby heeft een elegante syntax die natuurlijk leest en eenvoudig is om te schrijven.

Matz ontleende ideeën en uitdrukkingen van enkele van zijn favoriete programmeertalen ([Perl](http://en.wikipedia.org/wiki/Perl), [Smalltalk](http://en.wikipedia.org/wiki/Smalltalk), [Eiffel](http://en.wikipedia.org/wiki/Eiffel_%28programming_language%29), [Ada](http://en.wikipedia.org/wiki/Ada_%28programming_language%29), en [Lisp](http://en.wikipedia.org/wiki/Lisp_%28programming_language%29)) tot een nieuwe taal die [functionele programmatie](http://en.wikipedia.org/wiki/Functional_programming) balanceert met [imperatieve programmatie](http://en.wikipedia.org/wiki/Imperative_programming).

Het resultaat is een aantrekkelijke taal die heel natuurlijk aanvoelt. In de Ruby gemeenschap verwijzen we vaak naar de term POLS (Principle of Least Surprise). Het concept achter dit principe is heel eenvoudig: als je een minimum van Ruby kent, ben je niet verrast door de manier waarop de taal zich gedraagt.

## Adoptie ##{: #adoption}
Volgens de [TIOBE index](http://www.tiobe.com/index.php/content/paperinfo/tpci/index.html), zit Ruby in de top 10 van programmeertalen die wereldwijd wordt gebruikt. Een groot deel van de groei is toe te schrijven aan de populariteit van de software die is geschreven in Ruby, in het bijzonder het [Ruby on Rails web framework](http://rubyonrails.org).

## Sleutelelementen van de taal ##{: #key-elements}

> Ik wou een scripting-taal die krachtiger was dan Perl, en meer dan de object-georiënteerde Python.
> - Matz
{: cite=http://www.linuxdevcenter.com/pub/a/linux/2001/11/29/ruby.html}

* Alles is een object
* Alles is uitbreidbaar en kan gewijzigd worden
* Hoge code leesbaarheid

Voor meer informatie over de taal Ruby, bekijk de [Officiele Ruby programmeertaal website](http://www.ruby-lang.org/en/about).

## Code voorbeelden ##{: #code-examples}

**Print de string "Hello world" 10 keer:**

    10.times do
      print "Hello world!"
    end
    # => "Hello world!Hello world!Hello world!Hello world!Hello world!Hello, world!
    Hello world!Hello world!Hello world!Hello world!"
{:lang=ruby html_use_syntax=true}

**Conditioneel statement:**

	access_allowed = true if DateTime.now > DateTime.parse("2008-12-01")
{:lang=ruby html_use_syntax=true}

overeenkomstig met:

		if DateTime.now > DateTime.parse("2008-12-01")
		  access_allowed = true 
		end
{:lang=ruby html_use_syntax=true}

**Ternary operator:**

    age_classification = age > 12 ? "adult" : "child"
{:lang=ruby html_use_syntax=true}

overeenkomstig met:

    if age > 12
      age_classification =  "adult"
    else
      age_classification = "child"
    end
{:lang=ruby html_use_syntax=true}

**Array:**

	drinks = ["Coke", "Pepsi", "Orangina", "DrPepper"]
	#     => ["Coke", "Pepsi", "Orangina", "DrPepper"]
	# Access the Array instance
	drinks[0]     # => "Coke"
	drinks.first  # => "Coke"
	drinks.last   # => "DrPepper"
	drinks[3]     # => "DrPepper"
	drinks[-1]    # => "DrPepper"
	drinks[drinks.length - 1] # => "DrPepper"
{:lang=ruby html_use_syntax=true}


**Kijk of een item bestaat in een Array instance:**

	haystack = ["Mac", "NT", "Irix", "Linux"]
	needle   = "Windows"
	haystack.include?(needle)	# => false
{:lang=ruby html_use_syntax=true}

**Duw een item in een Array instance:**

	haystack = ["Mac", "NT", "Irix", "Linux"]
	needle   = "Windows"
	haystack.push(needle)
	# Or do it like this:
	haystack << needle
{:lang=ruby html_use_syntax=true}

**Definieer een methode:**

    def greet_visitor(visitor_name)
      "Hi #{visitor_name}!"
    end
{:lang=ruby html_use_syntax=true}

## Merb en Ruby ##{: #merb-and-ruby}

Merb probeert om zo dicht mogelijk bij de Ruby taal zelf te blijven. Daarom is het belangrijk te begrijpen wat wordt verstaan al de "Ruby Way".

Gedurende RubyConf 2008, maakte Matz volgende opmerking over Merb:

> Merb heeft een mooie toekomst voor de mensen die niet tevreden zijn met de vaste manieren van Rails.  Ik denk dat Merb gebruikers meer vrijheid zal geven in een Ruby-ish manier van programmeren
> - [Matz, auteur van de Ruby programming language](http://ruby-lang.org/){: .quote-author}
{: cite=http://merbist.com/2008/11/09/merb-1-0-released/}
