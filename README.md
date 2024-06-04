# Commands

- To configure cmake:

  `cmake -S . -B build`

- To build the project:

  `cmake --build build -j$(nproc)`
  OR
  `cmake --build build -j12`

- To run the tests:

  `GTEST_COLOR=1 ctest --test-dir build --output-on-failure -j $(nproc)`
  OR
  `GTEST_COLOR=1 ctest --test-dir build --output-on-failure -j 12`
