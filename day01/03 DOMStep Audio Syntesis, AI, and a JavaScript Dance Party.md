DOMStep: Audio Syntesis, AI, and JavaScript Dance Party
=======================================================

@jergason

## Web Audio API
Example:

    var c = new AudioContext();
    var n = c.createOscillator();
    n.frequency.value = 440;
    n.connect(c.destination);
    n.start(); n.stop(4);

## Audio Buffer
(see picture)

## Dropping the Beat
(see picture)

## Flocking
Set of rules that simulate the behavior of a flock.
Sync to beat:
    
    beatEmitter

setTimeout in Web Audio API has its own clock.

## Wob
(see picture)

Cool things
- flockingjs
- collaborative web audio editor by @thedeftone
- splice