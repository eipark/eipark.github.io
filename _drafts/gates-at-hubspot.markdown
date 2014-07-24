Gates are simply user settings with a key that allow us to control whether a user sees a feature. We can start a new feature, put it behind a gate and put it in production even before it's ready which allows us to test immediately. First, only HubSpotters are undated. Then when the feature is more mature, we ungate beta users, and then eventually, all customers.

In coffeescript, gated code is as simple as this:

```
if ungated['Version2OfSomeFeature']
    # show the user version 2
else
    # show the user version 1
```

We also have gating support in our Java code.
