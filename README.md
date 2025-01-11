# PHP Foreach Loop with unset() Bug
This repository demonstrates an uncommon bug in PHP related to the foreach loop and the unset() function. When using unset() within a foreach loop on an array, the loop's internal pointer might skip over elements unexpectedly.

## Bug Description
PHP's foreach loop uses an internal pointer to iterate through the array.  When you use unset() to remove an element, the internal pointer does not automatically adjust. This can lead to elements being skipped if they are adjacent to the element that was removed.   This issue is more subtle than a simple off-by-one error.