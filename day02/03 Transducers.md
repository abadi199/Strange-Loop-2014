Transducers
===========

Rick Hickey

## What are they?
extrace the essence of map, et al

## What kind of process
one that can ingest an input

## Transducer
reduce: lead back
ingest: carry into
transduce: lead accross
one the way back/in, will carry *inputs* accross a series of *transformations*.

## In real world
- put the baggage in the plane. as you do that
    - break apart pallets
    - remove bags that smell like food
    - label heavy bags
- And unspecified
- does baggage come/go on trolleys or conveters belts
    + rules don't care

## Transformation in the Programming World
collection function composition

    (comp
        (partial map label-heavy)
        (partial filter non-food?)
        (partial mapcat unbundle-pallet)) 

## Conveyences are everywhere
Rules only applies to 

## No reuse
Composed algorithms are needlessly specific and inefficient

*If you have something that talks about the steps, you can do the job, not the vice versa*

    (def process-bags
        (comp 
            (mapcatting unbundle-pallet)
            (filtering non-food?)
            (mapping label-heavy)))

mapcatting, filtering mapping return transducers.
[image]

## Transducible process
- intro, requence, transduce, chan etc accept transducer
- use the transducer to transform theri reducint function
- do their job with the transformed reducing function
- Many list fns can be defined in terms of foldr
    - encaluplates the recursion.
    - similarly via reduce (foldl)
[image]
[image]

### Transducers are fully decoupled
- know nothing about the process they modify

## Backwards comp

.
.
.
I'm lost