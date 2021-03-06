# Avoiding Common Attacks

The following attacks were prevented in the solution

### ShopKeeper

1. Re-entrancy attacks for withdrawals
2. Integer Overflow and Underflow via SafeMath on owner allocations
3. Contract text Drive-by-Injection (see main readme for details) (not so common)
4. Denial of Service by Block Gas Limit or startGas (limited amount of Shops and shop name length))  (This needs to be made better)
5. Denial of Service with Failed Call (all shops are managed on their own in order to let them run independently if needed)

### Shop

1. Re-entrancy attacks for withdrawals
2. Integer Overflow and Underflow via SafeMath on owner allocations
3. Contract text Drive-by-Injection (see main readme for details) (not so common)
4. Denial of Service by Block Gas Limit or startGas (limited number of products)) (This needs to be made better)


For both Shop and ShopKeeper, the unallocated funds will allow for any additional balance to be distributed. The only check around balance is on whether or not there are funds unallocated. Owners can only withdraw what is allocated to them and re-entry is prevented.

A small note on the Timestamp code used in the OwnerManagedLite implementation - it is set at an hour to not be an issue, but has been done in order to prevent a change being locked up (one owner griefing the others). That being said multi-sig also relies on some form of trust and that is something I am willing to discuss.

