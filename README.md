# simplerand
```cpp
#include <ctime>

#include <iostream>

#include "simplerand/simplerand.hpp"

int main() {
    simplerand::from_seed(static_cast<unsigned>(std::time(nullptr)));

    for (int i = 0; i < 10; ++i) {
        printf("%d\t %f\t %d\t %d\t %f\n",
            i,
            simplerand::gen(),
            simplerand::gen_bool(0.2f),
            simplerand::gen_range(0, 5),
            simplerand::gen_range(-3.0f, 3.0f)
        );
    }
    return 0;
}
```