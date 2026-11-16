# Issue

**Title:** Improving existing functions

## Description

I've worked on a couple of things here: 
* Changed how the `m_bio3d()` function is handled, which provides a 5x speed improvement when loading structures (especially obvious with multi-frame files).
* Re-order the arguments in `m_set_style()`, `m_add_style()` and `sel()` for quicker / easier defaults
* Added the `speed` option for `m_spin()`. 

To add the speed option, I had to change the actual `3dmol.js` library. I did this manually, including adding to the `*.min.js` libraries. I figure this is bad practice, but I didn't know how to go about it properly. The actual differences between the files are very minor (only 5 extra characters in the `*.min.js` files) but because it is on a single line it shows it as all different. 

The actual differences are as follows: 
#### Original
```js
this.spin=function(e){if(clearInterval($e),void 0===e&&(e="y"),"boolean"==typeof e){if(!e)return;e="y"}Array.isArray(e)&&(e={x:e[0],y:e[1],z:e[2]});var t=this;$e=setInterval(function(){t.rotate(1,e)},25)};
```

#### Changed
```js
this.spin=function(e,s){if(clearInterval($e),void 0===e&&(e="y"),"boolean"==typeof e){if(!e)return;e="y"}Array.isArray(e)&&(e={x:e[0],y:e[1],z:e[2]});var t=this;$e=setInterval(function(){t.rotate(1*s,e)},25)};
```

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `a7e9e36d24a0`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.