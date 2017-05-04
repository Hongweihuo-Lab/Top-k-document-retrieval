# Top-k Document Retrieval

    Top-k document retrieval is a full-text index. Given a pattern, it can be a word, a phase or 
    arbitrary substring, you can get the most relevant documents with it. 

## Reference

We used [simongog](https://github.com/simongog)'s [sdsl](https://github.com/simongog/sdsl-lite) library in
our code, and the [RMQ](https://github.com/hferrada/rmq.git) data structure implemented by Hector Ferrada and
Gonzalo Navarro.

## Requirements

* To compile the code, you need to install the [sdsl](https://github.com/simongog/sdsl-lite)
  library.
* `g++`version 4.9 or higher.

## Installation

To download and compile the code use the following commands.

```Bash
git clone https://github.com/pucika/top-k-document-retrieval
cd top-k-document/src
make
```

## Example

The doc/ directory contains the document set.

```cpp
#include <iostream>
#include "gst.h"

using namespace top_k;

int main(int argc, char* argv[])
{
  GST gst;
  gst.constructure("../docs/");
  string pattern;
  int k = 0;
  while(true) {
    getline(cin, pattern);
    std::cin >> k;
    std::cin.ignore();
    get.search(pattern, k);
  }
  return 0;
}
```
## Contributors
### Code
•	Dongliang Zhang （张栋梁）
### Paper
It is an implementation of the paper.

Wing Kai Hon, Rahul Shah, Sharma V. Thankachan, & Jeffrey Scott Vitter, Space-efficient frameworks for top-k string retrieval, Journal of the ACM (JACM), 2014, 61(2): 9.
