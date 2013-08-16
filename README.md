Purpose
=======

The purpose of the idn-properties tool is to list a summary
of the codepoints in the provided file. Input files can be
formatted as RFC 4290 tables, RFC 3743, or just any text file
containing a table of Unicode codepoints in the format of
U+[A-Z]+.

Usage
-----

The output is a summary of scripts being used, and a summary
of the derived properties as concluded by the IDNA2008 algorithms.
(PVALID, DISALLOWED and so on.)

Example usage:

    $> idn-properties --files example-tables/se-yiddish.txt
    Reading allcodepoints.txt
    Reading Scripts.txt
    # Properties
      PVALID: 45
    
    # Sscripts
      Common: 11
      Hebrew: 34

A complete extended table with the derived and script properties
can be output using the --reportDir file option.

Testing based on
----------------

All testing is done based on Unicode 6.2 and IDNA2008.

The table codepoints.txt was generated with the ruby program createtables
found here: http://stupid.domain.name/idna
(Thanks to Patrik Fältström)

The Unicode source files can be found here:
http://www.unicode.org/Public/6.2.0/ucd/

The Unicode Script file can be found here:
http://www.unicode.org/Public/6.2.0/ucd/Scripts.txt

/ Patrik Wallström, pawal@iis.se

Thanks for support:
Cary Karp
Patrik Fältström
John Colosi
