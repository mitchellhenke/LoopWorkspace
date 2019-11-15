# LoopWorkspace

# ABOUT THIS BRANCH

This branch is based on the work done here:

https://github.com/LoopKit/Loop/pull/849

https://github.com/LoopKit/Loop/pull/726

https://github.com/LoopKit/LoopKit/pull/246

that add Integral Retrospective Correction and Fat/Protein Unit functionality.


### FPU

Making FPU work in Loop is not straightforward, and is currently something of a workaround.  The FPU changes prompt for grams of carbohydrate, fat, and protein when adding a meal, and converts that into two carbohydrate entries in Loop.  One for the grams of carbohydrates entered on a 2 hour duration, and a second delayed one that converts the fat and protein into carbohydrates in an amount and duration specified by the research linked in the pull request above.  The delay and fat/protein:carbohydrate ratio are configurable.

The above means that when a meal is saved, it will be entirely in carbohydrates, and any reference to the original fat/protein is lost, so editing entered meals is confusing.

## Clone

This repository uses git submodules to pull in the various workspace dependencies.

To clone this repo:

```
git clone --branch=mitchellhenke-rsilvers-fpu-irc --recurse-submodules https://github.com/mitchellhenke/LoopWorkspace
```

Replace `<branch>` with the initial LoopWorkspace repository branch you wish to checkout.

## Open

Change to the cloned directory and open the workspace in Xcode:

```
cd LoopWorkspace
xed .
```

## Build

Select the "Loop (Workspace)" scheme (not the "Loop" scheme) and Build, Run, or Test.

<a href="/docs/scheme-selection.png"><img src="/docs/scheme-selection.png?raw=true" alt="Image showing how to select the Loop (Workspace) scheme in Xcode" width="400"></a>

