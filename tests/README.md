Tests
=====

 generate-regular-expressions:
  Example script utilizing the `abnf` ruby module from 
  http://www.a-k-r.org/abnf/ and https://github.com/akr/abnf that converts
  ABNF formal definitions to regular expressions ("so now you have two
  problems!").

 generate-sample-test-data:
  Example script utilizing the `abnfgen` C utility to automatically create
  test data for each entity defined within the ABNF (including ontological
  entities).

Outstanding
-----------
 * Generate further tests, including command line sanity tests of entity 
   values and/or regular expressions for such, utilizing the perl modules
   `ABNF::Grammar`, `ABNF::Validator` and/or `Parse::ABNF`.
     * There's also a tool `abnf2c` (depending on a library `librfa`)
       however they are apparently not maintained and don't seem to want
       to play anymore :(
