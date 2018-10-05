
We use these criteria from the Google Test Blog:

https://testing.googleblog.com/2010/12/test-sizes.html

    Feature                 Unit         Integration           End to End

    Network access          No           localhost only        Yes
    Database                No           Yes                   Yes
    File system access      No           Yes                   Yes
    Use external systems    No           Discouraged           Yes
    Multiple threads        No           Yes                   Yes
    Sleep statements        No           Yes                   Yes
    System properties       No           Yes                   Yes
    Time limit (seconds)    60           300                   900+

The time limits are not hard and fast rules. That said, if a single unit test takes 15 seconds to complete, then it should probably be in its own test suite.

