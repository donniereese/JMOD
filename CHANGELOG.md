Changelog

alpha1.3.1
- Implemented Basic and "Dynamic" blocks
- Implemented support for RotaryCraft SurrogateBedrock on Dynamic Blocks
- Implemented support for ReactorCrafy NeutronShield on Dynamic Blocks
- Implemented support for Redstone Power on Dynamic Blocks
- Implemented first step of the EventSystem
- Introduction of ISettingsReceiver and ISettingsProcessor, part of the syntax rewrite
- Implemented Plugin System
- JMOD is now DEPENDENCY FREE (but the plugins ofc are not)
- Implemented ASM Transformer loading from plugins
- revamped internal mod configuration (to allow plugins to add their own config)
- Implemented several hooks into plugins to perform specific actions (like patch tools, determine the repair value of a tool, etc) on their own merit
- Implemented FuelHandler for JMOD (needs some more work to compensate for MC(F)s wonky burnTime code )
- jmods can now contain plugin code and vice versa
- The Discoverer now also follows symbolic links. Penguins rejoice!
- Adjusted execution priorities to make sure Fluids are created before items (like buckets)
- Implemented generic buckets (CoreBucket)
- R.I.P. ItemWoodenBucket
- CoreBuckets now work with IFLuidHandler TileEntities
- Now uses MCF'S EventBus to let Plugins do their jobs
- Items can now have a "container" and decide leave their container in the crafting grid after crafting
- Items can now contain them"self" to allow for "crafting tools" like HarvestCraft does a lot of
- Introduced the Action "SetItemProperties" to adjust the values: stackSize, container and durability
- stringToItemStackOrFirstOreDict now supports oredictvalues with a stacksize modifier (for example "ingotCopper@16")

alpha1.3.0 (off-commit)
- Lots and lots of groundwork for later changes, including the upcoming EventAPI

beta1.2.2 (LTS release)
- fixed comparision of ItemStacks by oreDict membership. Fixes (among others) [Issue #41](https://github.com/SvenKayser/JMOD/issues/41)
- Switched json parsing (back) to GSON, now with regex based  comment stripping [Issue #38](https://github.com/SvenKayser/JMOD/issues/38)

beta1.2.1 (LTS release)
- Implemented proper support for ingredient based search for Shaped StringRecipes for NEI [Issue #31](https://github.com/SvenKayser/JMOD/issues/31)
- fixed RoC blast furnace handler not executing [Issue #32](https://github.com/SvenKayser/JMOD/issues/32)

beta1.2.0 (LTS until Mar 31st 2017)
- Added support for RotaryCraft PulseJetFurnace and Compactor
- Fixed some RotaryCraft script bindings cause crashes when used without RotaryCraft present
- Added support for RotaryCraft DryingBed, RockMelter and Liquefaction (Wetter)
- fixed hardness and opacity not being handled by SetBlockProperty
- fixed inconsistency between servers and clients executing SetBlockProperty
- fixed, streamlined and improved armor repair code (now works with both items and oredict entries)


alpha1.0.5 (no release)
- fixed crafting spam and resulting performance bumps [Issue #17](https://github.com/SvenKayser/JMOD/issues/17)
- fixed fluids
- RoC Centrifuge cleanup 
- merged and up-ported AppleCore support, credit to nmarshall23 [PR#10](https://github.com/SvenKayser/JMOD/pull/10)
- cleaned up startup ordering, fixing [Issue #8](https://github.com/SvenKayser/JMOD/issues/8)
- fixes I forgot about


alpha1.0.4 (no release)
- implemented Fluids + Fluid API [Issue #16](https://github.com/SvenKayser/JMOD/issues/16)
- implemented interface for sifting results (ExNihilo) [Issue #12](https://github.com/SvenKayser/JMOD/issues/12)
- implemented Centrifuge API (RotaryCraft)
- much re-organization
- streamlined loading stage distribution to the actions
- tons of changes under the hood


alpha1.0.3 (released)
- the JMOD jar is now executable and provides a simple .jmod validator
- Improved Nashorn's binding of the ScriptingObject
- Hooked scripts earlier into FML's loading process
- Improved loading performance again (to the point where JMOD is actually waiting on minecraft, instead of the other way around)
- The Loader now performs a rudimentary sanity check to prevent stupid jmods from doing stupid things
- Fixed AddSmeltingRecipe being invalid by default
- Fixed not executing RemoveSmeltingRecipes
- Fixed eval error line numbers not working (again...)


alpha1.0.2 (no release)
- JMOD is now a core mod only
- Improved loading performance
- Added sanity check for StringListRecipes
- Fixed crash when encountering missing metal blocks/ingots
- Fixed creative tabs not ready on time
- Fixed Action priority
- Fixed OreGen not running concurrently


alpha1.0.1 (no release)

- First Version, rewrite from the base of the si.core mod


