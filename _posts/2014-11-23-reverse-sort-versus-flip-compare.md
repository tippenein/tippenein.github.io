---
layout: post
title: Comparing reverse sort and flip compare
---


GHCmod-vim hinted at an improvement in some code I was writing:

`reverse $ sort` why not `sortBy (flip compare)`

So I looked at the type signatures for each of these.

```ghci
> :t reverse $ sort
> Ord a => [a] -> [a]

> :t sortBy
> (a -> a -> Ordering) -> [a] -> [a]

> :t (flip compare)
> Ord b => b -> b -> Ordering
```

`flip` is just `f x y = f y x`

A little reminder of how `compare` works:

```ghci
> compare 1 2
> LT
> flip compare 1 2
> GT
```

This is the part that wasn’t obvious to me; that by simply flipping the
comparison we’re reversing the resulting sorted list.
At that point we can see that `sortBy` is traversing the list once whereas
`reverse $ sort` is running through the list twice.

