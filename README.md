# utl-resolve-macro-variable-within-single-quotes
Resolve macro variable within single quotes
    Resolve macro variable within single quotes

    github
    https://github.com/rogerjdeangelis/utl-resolve-macro-variable-within-single-quotes

    SAS Forum
    https://tinyurl.com/vh4efhk
    https://communities.sas.com/t5/SAS-Programming/I-need-to-resolve-macro-variable-in-single-quotation/m-p/610384


    Problem:

         %let name=jhonson;

         Data want;
         Myname=%str('&name') ;
         Run;

     I get

       Up to 40 obs WORK.WANT total obs=1

       Obs    MYNAME

        1     &name

     I want

       ORK.WANT total obs=1

       Obs    MYNAME

        1     jhonson

    *          _       _   _
     ___  ___ | |_   _| |_(_) ___  _ __
    / __|/ _ \| | | | | __| |/ _ \| '_ \
    \__ \ (_) | | |_| | |_| | (_) | | | |
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|

    ;

    Data want;
      Myname=resolve('&name') ;
    Run;

