A C++ program that convert from Felix's connection vector format to a format more
suitable for reading by tmix-ns
  - replaces t, >, < lines with line with format:
  * {I,A} - initator or acceptor
  * time to wait after sending (usecs)
  * time to wait after receiving (usecs)
  * bytes to send (if 0, send a FIN)
