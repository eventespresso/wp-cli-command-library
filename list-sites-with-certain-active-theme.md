## Command

This command will spit out a list of all sites on a WordPress network that have the named theme active.

```
wp site list --quiet --field=url --skip-plugins | grep "http" | xargs -r -d '\n' -n1 -I{} sh -c 'wp theme is-active baskerville --url={}; echo $? = {};' | grep "0 ="
```

In the command above a **baskerville** theme is used as an example. Replace **baskerville** with any theme you wish to search for.


### Sample Output

```
0 = http://nazartests.makeeventsnotwar.com/
```

### Variations

_In this section could go any possible variations of the command_