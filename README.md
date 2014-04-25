# Reachability Helper

## Requirements

[https://github.com/tonymillion/Reachability](https://github.com/tonymillion/Reachability)

      //Initialize
      [TLIReachabilityController sharedController];

      //NSNotification example
      [[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(reachabilityDidChange:) name:kReachabilityChangedNotification object:nil];

      - (void)reachabilityDidChange:(NSNotification *)notification {
            Reachability *reachability = (Reachability *)[notification object];

            if ([reachability isReachable]) {
              NSLog("Reachable");
            } else {
              NSLog(@"Not reachable");
            }
      }
