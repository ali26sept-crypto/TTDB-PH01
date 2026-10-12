# project progress
### oct 3rd 2026
1. downloaded linux on my system and did the set up for g++ compiler boht hii koi crazy kaam hogaya hai mushkil tha but apna yk sab sa pehle toh ghabrana nahi ha
2. also tried my best to understand the constant variables provided in the server.cpp kch na kch toh smjh aa hii gaya tha baki allah ka hawalay
3. also implemented the stack structure with node struct in it bhaisab boht hii crazy cheez thi yeh toh 
# project progress
### oct 4th 2026
1. wrote the reading line function that will read the each line that will be presenr in the source.bin file that is being passed to us from the client
2. wrote first word function isma jo bhi line huma recieve hogi uski tokenization ka through ignoring the leading spaces we will find the start and end of the first word and will return it through the function
3. wrote the second word function iska pehlay part ma copy paste kiya first funtion ka process becos of obvious reasons bruh and then calculated the second word through the same process i calculated the first word crazy calculation thing hogai ha bhaijannn
4. also inplemented the valodation wala function for function for our world class out of the world coding language C-- it was very simple tbvh used the first word function to valudate the start of the line for function initialization or ab zara bas hogai ha toh baki baad ma thanks.
### Pass 0x1: Record Layout & Resolution (`resolve.bin`)
* Implemented `writeResolveRecord` to write binary records in `[offset(8B)][size(4B)][string]` format.
* Implemented `readResolveRecord` to read records sequentially from the binary stream.
* Implemented `resolveProgram`:
  * Pass 1: Stored raw lines into `resolve.bin`, tracked `func` positions in `funcArray`, logged pending `call` locations in `patches`, and checked for `main`.
  * Pass 2: Backpatched target function file offsets into the corresponding `call` record headers.

### Pass 0x2: Execution Setup
* Implemented `tokenizeLine` to categorize words into `KEYWORD`, `IDENTIFIER`, and `PARAM`.
* Implemented custom linked `Stack` methods (`push`, `pop`, `peek`, `isEmpty`, `snapshot_into`).
* Implemented `buildSnapshot` to dump stack frames into snapshot records.
## Remaining Work
* Complete `executeProgram` in Pass 0x2 (instruction dispatch for `set`/arithmetic, handling call frames, and capturing snapshots to `Timeline`).
* Implement Pass 0x3 (`writeTdbg`) to serialize snapshots and write the dense index table to `session.tdbg`.
