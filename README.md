![General Assembly Logo](http://i.imgur.com/ke8USTq.png)

# Ruby Enumerables IO

## Instructions

Fork, clone, branch (training), and bundle install.

## Objectives

By the end of this lesson, students should be able to:

-   Iterate through a file one line at a time.
-   Explain why you should only use the block form of `File.open`.
-   Load data using the CSV library in order to create Ruby objects.

## Introduction

In Ruby, files, and all IO streams, are Enumerable.

## Files as lists

Ruby's [File](http://ruby-doc.org/core-2.3.0/File.html) includes `Enumerable` so
 we can use all of its methods to process files a character or a line (the
 default) at a time.

Other enumerable classes related to working with files include [IO](http://ruby-doc.org/core-2.3.0/IO.html),
 and [Dir](http://ruby-doc.org/core-2.3.0/Dir.html).

I used the Ruby Standard Library class [CSV](http://ruby-doc.org/stdlib-2.3.0/libdoc/csv/rdoc/CSV.html)
to load data for the `bin/*_array.rb` scripts.

### Code along - read a file

Using `bin/read_file.rb` we'll read all the lines in a file and print them.

### Lab - count characters, words, and lines in a file

Let's create a script to mimic the behavior of the `wc` (word count) command
 line utility in `bin/word_count.rb`.

## CSV files

A file containing Comma Separated Values (CSV) is a simple and well supported
 format for data interchange, especially for tabular data.

### Code along - CSV

We'll build a data loader for pets in `lib/pets.rb` using the Ruby standard
 library class [CSV](http://ruby-doc.org/stdlib-2.3.0/libdoc/csv/rdoc/CSV.html).

We'll use a `lambda` - shorthand syntax `->([args]) {[code]}`, see [Proc](http://ruby-doc.org/core-2.3.0/Proc.html) -
to ensure we use symbols as keys when loading data.
In Ruby, lambdas verify the number of arguments.

## Challenge

Read two files at the same time using `bin/read_files.rb`.

Look at [Enumerator](http://ruby-doc.org/core-2.3.0/Enumerator.html) which is
 what gets returned when we call `each` on an open file without a block.

We'll need to look briefly at exception handling as Enumerator relies on this
 mechanism.

## [License](LICENSE)

Source code distributed under the MIT license. Text and other assets copyright
General Assembly, Inc., all rights reserved.
