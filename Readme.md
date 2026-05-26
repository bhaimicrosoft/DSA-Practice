# DSA Practice

A C++ workspace for practicing Data Structures and Algorithms problems with a streamlined local development setup using VS Code.

## Setup

### VS Code Snippet (`cpp.json`)

A custom snippet is configured to quickly scaffold new solution files. To use it, type `BoilerPlate Code` in any `.cpp` file and press Tab.

**Location:** `File > Preferences > Configure User Snippets > cpp.json`

```json
{
  "boilerplate": {
    "prefix": "BoilerPlate Code",
    "body": [
      "#include \"bits/stdc++.h\"",
      "using namespace std; \n",
      "int main()",
      "{",
      "    #ifndef ONLINE_JUDGE",
      "    freopen(\"input.txt\", \"r\", stdin);",
      "    freopen(\"output.txt\", \"w\", stdout);",
      "    #endif",
      "\t",
      "\treturn 0;",
      "}"
    ],
    "description": "This is a CPP starter code"
  }
}
```

### Generated Boilerplate

The snippet expands to:

```cpp
#include "bits/stdc++.h"
using namespace std;

int main()
{
    #ifndef ONLINE_JUDGE
    freopen("input.txt", "r", stdin);
    freopen("output.txt", "w", stdout);
    #endif

    return 0;
}
```

### How It Works

- **`input.txt`** — Place your test input here.
- **`output.txt`** — Program output is written here.
- The `ONLINE_JUDGE` guard ensures file I/O is only used locally. On competitive programming judges, standard I/O is used instead.

### Build & Run

The default build task compiles and runs the current file with `g++ -std=c++20 -O2`:

```
Ctrl + Shift + B
```

Output executables are placed in the `output/` directory.