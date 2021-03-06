# Design pattern decisions

The following patterns were implemented in the solution:

### ShopKeeper

1. Circuit breaker with activate/deactivate via the OwnerManagedLite contract
2. Withdrawal pattern when owners take funds (allocated in a separate call)
3. Restricting access via the OwnerManagedLite contract
4. Small state machine for multi-sig changes to the contract owning state
5. Shops are created via a factory (not the current EIP Factory pattern) and are accessed directly not via ShopKeeper - ShopKeeper is merely a lookup to it
6. An initial upgradable contract was used, but was removed as I had some issues with it


### Shop

1. Circuit breaker with activate/deactivate via the OwnerManagedLite contract
2. Withdrawal pattern when owners take funds (allocated in a separate call)
3. Restricting access via the OwnerManagedLite contract
4. Small state machine for multi-sig changes to the contract owning state

