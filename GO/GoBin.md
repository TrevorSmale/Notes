# Go Binaries

### Why Go Executables are so damn big

Go binaries are standalone
Everything is statically linked
Memory management
Symbol tables
External packages

The size of the Bin can be reduced by removing debug and symbol table data

Downsides

May cause bugs when:
working with reflections
working with servers and HTTP

### Packaging

Go projects can be packaged into single executable binaries.
Go is also capable of building other frameworks into the binary.
REACT front end applications can be packaged with GO and a Database to form a full application.
PocketBase is a great example project that combines Svelt + REACT + GO + SQL LIGHT to form a full service package including payment processing.

#### Be aware of

CG enabled option
