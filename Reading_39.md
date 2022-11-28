Dean Weiss
28 November 2022

# SQli with Burpe, WebGoat

<p>
In particular, if you’re a sysadmin in any moderately sized organization, there are probably a half dozen internal applications that your company depends upon day in and day out which:

- Are presumed to be internal, so security isn’t a big priority.
- Were developed a decade or more ago when some security development practices weren’t as ingrained.
- Will quite likely crash if you run even an “innocuous” SQL injection attack against them. For instance, you can often grind a database and web server to a halt simply by requesting all of the records in the database instead of the 1 record that the application page would typically load.

One of the really remarkable things about SQL is that the basics of the language haven’t changed much since it was first invented in the early 1970s. While some of the more esoteric commands differ between the major database vendors and open source options, the basics are the same across almost everything.

In a database, these lists are called tables – and they’re the fundamental building block of how data is structured in a database. At its core, a table is simply a list of information.

I find that it’s sometimes helpful to think of database tables like sheets in a spreadsheet. Each sheet is the list and the columns in that sheet are the attributes of the items in that list.

  
  
</p>

source: https://www.varonis.com/blog/sql-injection-identification-and-prevention-part-1
