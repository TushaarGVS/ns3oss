A C++ program that convert from Felix's connection vector format to a format more
suitable for reading by tmix-ns
  - replaces t, >, < lines with line with format:
  * {I,A} - initator or acceptor
  * time to wait after sending (usecs)
  * time to wait after receiving (usecs)
  * bytes to send (if 0, send a FIN)

 EXAMPLES:
 
  > 826 \t            I   0    0    826 \n
  t 534  \t           A   0    534  1213 \n
  < 1213 \t           A   872  0    0 \n
  t 872

  c< 190 \t           A   0    0    190 \n
  t< 505  \t          I   0    0    396 \n
  c> 396  \t          A   505  0    46 \n
  t> 6250 \t          I   6250 0    0 \n
  c< 46
