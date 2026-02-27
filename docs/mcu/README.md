# Microcontroller Unit

This is going to be the heart of the player, for this reason it's important to analyze what we need and don't need. For one, this is a hobby project so we're limited by packaging formats. LQFP and LQFN are wwhat we're going to be using throughout this design because it's easier (not easy) to assemble. We're also avoiding over-powered SOCs for what we need. The STM32 model we fell on is the STM32H7B0 line.

### Features We Liked:
- LQPF packaging
- Built-in LCD controller
- Dual SD MMC interfaces
- 1.4 MB of on-chip RAM
- USB 2.0 OTG support
- SAI interface
- Efficiency
- Good documentation
- Good support
- Good stock

## Concerns

While this chip is incredible, the package has limitations. There are 4 models of the H7B0 in the LQFP packaging. Those are the 64-pin, 100-pin, 144-pin, and 200-pin versions. The 64 in particular has limitations that the others don't see. The 100 has some of the features the 64 lacks but is still not as full featured as the 144 and 200 pin versions, for obvious reasons. Our aim is to use the 100 in a worst-case scenario but preferably the 64-pin as the LQFP packaing limits us in how much space it'll take up on the PCB which is very important when considering keeping this device as thin as possible.

The 64- and 100-pin versions are referred to as the H7B0RB and H7B0VB respectively and are referred as so in the STM32H7B0 datasheet. Pages 7 through 9 outline the key differences between all of them. Particarly, the SMPS chips are all FBGA while wht Non-SMPS are all LQFP. The lack of an SMPS step-down converter doesn't really limit our current design but we'll see in the future.
