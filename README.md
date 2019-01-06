# GHCJS Spike

Explore practicality of GHCJS is for use in:

- AWS lambda functions
- Web pages


## Things I care about:

- executable size
- speed of runtime initialization
- access to AWS services
- ability to wrap/integrate existing node/npm stuff
   - GraphQL
   - React
   - Browser APIs


## How I got it working journal

0. create directory and simple `stack.yaml` per stack web site
0. create a simple `package.yaml` and source files too
0. `stack setup`
0. it's missing cabal so from outside the directory, `stack install cabal-install`
0. `install hpack` since the specified lts doesn't use it
0. that didn't work because of dep things so edit `~/.stack/global-project/stack.yaml`
   and set resolver to match the same one i put in the project `stack.yaml` (7.19)
0. `install cabal-install` again from outside the directory
0. `install hpack`
0. `install happy`
0. `install alex`
0. `install hscolour`
0. `install hsc2hs` that didn't work, ignore for now
0. go back into directory and `stack build`
0. whoops, didn't run `hpack` first so it's just building a bunch of stuff.
   I don't know if it's building everything in stackage or if it's just builing
   enough for the prim and prelude. whatever i'll wait. it's repeatedly saying
   something about 'Booting GHCJS (this will take a long time)' so I figure it
   is stuff that will be needed evenrually.
0. It _is_ taking a long time. see you back here in a while...






