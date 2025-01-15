# MongoDB $inc Operator: Unexpected Behavior with Negative Values

This repository demonstrates an uncommon bug related to the MongoDB `$inc` operator when used with negative values.  The issue arises when decrementing a counter that might already be zero or doesn't exist.  The default behavior doesn't raise an error but can lead to unexpected results in the counter.

## Bug Description
The code attempts to decrement a counter using `$inc` with a negative value.  If the counter is initially 0 or doesn't exist, the intended behavior is to either keep it at 0 or create it with a value of 0, but it might fail silently or produce unintended results.