# Changelog

## [1.0.2](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.2.0...v1.0.2) (2026-11-15)


### ⚠ BREAKING CHANGES

* **no-external-store-subscription:** new recommended rule
* **no-empty-effect:** remove rule ([#67](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/issues/67))
* **no-pass-ref-to-parent:** remove rule
* false negatives when references were composed of a combination of state/props/refs upstream, not just one
* shorten name of no-adjust-state-when-a-prop-changes and no-reset-all-state-when-a-prop-changes
* **no-adjust-some-state-when-a-prop-changes:** remove inaccurate "some" from name
* **no-pass-data-to-parent:** add rule

### Features

* add isReactFunctionalHOC utility function for HOC detection ([960bb68](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/960bb6812ea7fecc676b4822d17bdee6f09f43ab))
* add more context to messages for clarity and actionability ([877f436](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/877f436cc2b4588ba235c1bad6e99248769c8ca4))
* flag most rules when *any* - not *all* - upstreams are internal ([6e2b73d](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/6e2b73d8b5a328143833ff56142856dae33ba3db))
* follow call chains involving aliases ([4b7ef19](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/4b7ef196844578f6db385023c3ca0370bfe85681))
* follow named functions passed to `useEffect`s ([093cadb](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/093cadb84ebfcc71e68eb8a1c189776fc8226586))
* more idiomatic recommendation for passing to parent inside custom hooks ([15f2681](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/15f2681c37da62a688b7d33865fd0bfc09816a3c))
* **no-derived-state:** remove `avoidSingleSetter` case ([9d14903](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/9d149032853c8453f15edf62ec66f1efcb39a622))
* **no-derived-state:** separate message for single setter anti-pattern ([0cb291c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/0cb291c119131574f252394a34324c766f759924))
* **no-empty-effect:** flag effects with no args ([9282182](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/92821820532c8bc273a8f45306960c93220bd285))
* **no-empty-effect:** remove rule ([#67](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/issues/67)) ([ce0678a](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/ce0678a32f0243150852d48b9f9548b52b654648))
* **no-event-handler:** flag props ([8a241fd](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/8a241fd60e7a0075aac6774fabad3819b9b55f5c))
* **no-external-store-subscription:** new recommended rule ([61e7f60](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/61e7f60d0665e3ba2c76bc168f972eeba42ee6af))
* **no-initialize-state:** add arguments to message ([11d01f2](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/11d01f2d528fc9489a398e04f7f097288a799748))
* **no-initialize-state:** advise to prefer `useSyncExternalStore` for SSR components ([f36d88a](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/f36d88ab13aaa66b651e135804f33a604962d8fd))
* **no-pass-data-to-parent:** add rule ([6d1d84f](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/6d1d84f16f980a49abd0b8ccb7bcf589b2b1cd9c))
* **no-pass-data-to-parent:** flag non-direct calls ([e6923f2](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/e6923f296378c004e995435c0a9dcce2939e33d2))
* **no-pass-data-to-parent:** flag passing literals ([c1226f1](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/c1226f1ebb571d273529cd96243888bbe82f86fb))
* **no-pass-live-state-to-parent:** narrow check to passing state ([cb39f62](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/cb39f6288af0f217c741f4fd65b7f4b20a8a15b4))
* **no-pass-ref-to-parent:** new rule, and skip ref event handlers in no-pass-data-to-parent ([031ee61](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/031ee61cb197beb5dd15d40cd0b34a2f1125d9aa))
* **no-pass-ref-to-parent:** remove rule ([6149ae7](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/6149ae735b80c530aa8599127cc20bfa7d560353))
* see through TypeScript-only syntax ([29c115e](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/29c115e42502cfcd3656adc33edcca4c726c450c))
* strict config ([9fef80c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/9fef80ce3d292c95dc7350dd6aa389d00e493486))
* support popular third-party effect wrappers ([c62dbd3](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/c62dbd3013dbeeffffb26cc56f12516a824eaef2))
* support renamed React hook imports ([e77d3ec](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/e77d3ec5fd88a4b076663cf7b5d790f88894bb36))
* treat context values as props ([8a89798](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/8a89798106857c563b41a76df3f5490aec45a89c))


### Bug Fixes

* add `homepage` and `bugs.url` to package.json ([da40508](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/da4050898ef9db46f98353b4675ddfc616f6a6c5))
* allow isHOCProp to accept both React.memo and memo ([960bb68](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/960bb6812ea7fecc676b4822d17bdee6f09f43ab))
* analyze `const Component = function() {}` components ([88faa83](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/88faa830900e235506616a730b3330d2cedd49a7))
* analyze both derived setter and eventual setter args ([f737f8b](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/f737f8b07b21c0d8ad7de073d59f93878c2e6b69))
* analyze effects with omitted or variable deps ([60db4c5](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/60db4c585ac377d94ab634d588af6ebe5cf3ede8))
* **config:** name the flat configs ([dd8783c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/dd8783cba298e841ce4b6d3a47b70f7cf924fe05))
* **config:** stop adding files to the lint set ([365be79](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/365be79fd6aa27c28fcb9c974065d57b64d67bdb))
* correct eslint peerDependency version ([19748f1](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/19748f1db4002e9a8d1062e0010c82560a9efb52))
* descend into `FunctionDeclaration` bodies ([7ceb417](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/7ceb417cf44a120a9ad81651fbb10a825426cb8b))
* detect separately-wrapped HOCs and their props ([68f14dd](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/68f14ddbff74a850bb7542eb11901ec2b4be3ff5))
* detect state setter and prop calls via intermediate variables ([b0e49ec](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/b0e49ec1f57c193d6ddb592dfa4cc347b04a3838))
* do not analyze async IIFEs ([58e31bd](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/58e31bd87d3b6f3657fafe89a15ecdf90ee29aca))
* do not analyze useLayoutEffect - they are likely valid ([cb3af77](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/cb3af77b3a61e42364efec018cbecd14b132fc35))
* do not flag calls inside named functions (especially async) ([b6f952c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/b6f952c53f700ad07e2af357f148041f80707ca9))
* don't analyze calls to externally-defined async functions ([76f43ec](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/76f43ecd67641e53f3dddbbefc99c4d032f29088))
* don't bundle dependencies into dist version ([#45](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/issues/45)) ([91f7244](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/91f724446fd89c94948a97718493f5e0468b2147))
* don't fall-through to entire enclosing body when `useEffect` fn arg is opaque ([691c9c0](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/691c9c0760d1ba7505ebc24f1f14a462bb172da1))
* dont consider calls to be prop callbacks when they merely receive a prop arg ([8f1edde](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/8f1eddeef8a68b88c8eb3dfcf652d25e7f04a0e9))
* false negatives when references were composed of a combination of state/props/refs upstream, not just one ([a43f681](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/a43f68184f06e8396192e92245e8e6c1bfb09197))
* follow member access on aliases ([8624081](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/86240813e187e5510fe2d717c515b70e5e4caf2e))
* follow only stable, invoked aliases in call chains ([485d5e9](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/485d5e98625c18664ddd352b144ab38b14e998c5))
* handle defaults in useState destructuring ([bd85422](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/bd85422b78d527efab94e0819b4616df8b45a87e))
* ignore arguments to upstream calls when searching for state/props ([cb8d97f](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/cb8d97fbf8efa357f03a2db02086e5377946565f))
* ignore effects with cleanup ([df19ac0](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/df19ac015052e9407051995902c080f10dcbff80))
* ignore non-function effect callbacks ([f31723c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/f31723c540e4ce4e149fb13aa0e7ea023b4619d1))
* ignore setter calls in cleanup function and more generally ([86cd45b](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/86cd45b14d007c55951274f45c8a9b5ea7e1eb18))
* lint error before building ([dca08d1](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/dca08d15763358c04ef1ff0d7a4092423cf21ce2))
* **no-chain-state-updates:** do not flag when responding to prop changes ([a28d102](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/a28d102e6397c3c51d91ae068c729d027232a894))
* **no-derived-state:** account for non-calls when flagging single setter calls ([6bd1ef3](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/6bd1ef30dd957b76601aaa52a4083f891c886844))
* **no-event-handler:** flag at usage instead of declaration ([f55df2d](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/f55df2d85813326b20991590df5d711b9960f6c8))
* **no-initialize-state:** analyze effects that only have setter in deps ([41fccc1](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/41fccc18cc7b9cf5cdefcd1507839f7fc8f15f0a))
* **no-initialize-state:** treat aliased setters in deps as setters ([9de2e7d](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/9de2e7dfc8a699271c5de6e33d91e489f9fc50c8))
* **no-manage-parent:** don't flag when non-prop in deps ([1832c3a](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/1832c3aecbe567c1890479e4c763237dd0e4ede0))
* **no-pass-data-to-parent:** remove duplicated quotes from message ([56f410b](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/56f410b47643a3f87ca6850d83c52bc21eb7b546))
* **no-pass-live-state-to-parent:** remove duplicated quotes from message ([5e6cc16](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/5e6cc164f4fe33b9222d856d083658c619623088))
* **no-reset-all-state-on-prop-change:** count useState calls instead of state reads ([6ea7641](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/6ea7641adc71e6041fe75e57bc4225e269956a1d))
* **no-reset-all-state-on-prop-change:** don't crash when can't find containing component/hook ([e7b2158](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/e7b21583dfb553647da89a5a77a505cbc8da404f))
* **no-reset-all-state-on-prop-change:** false negatives on custom hooks ([d80697d](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/d80697d0e73cf61b07ee6f2e1b723e0b11b8f4dc))
* **no-reset-all-state-on-prop-change:** flag when the same setter is called twice ([2f2aa4e](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/2f2aa4ed4a14e348f1158df563833cd9f3f61c53))
* **no-reset-all-state-on-prop-change:** handle wrapper setters ([5104d25](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/5104d25228854546ce20375159698a79413c4bef))
* report the written state for wrapper setters ([45e37b6](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/45e37b6b73587a717703dcee2bb50c1d823780e7))
* stack overflow when effect has recursion ([98d5e0c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/98d5e0c97dac518659fa64d5da0de6ae56c4449b))
* stop defining/recommending browser globals for consumers ([e61af56](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/e61af56a4c61e928e195d46b1219e973bad5db7f))
* stricter criteria for whether something is state ([cd33b9c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/cd33b9cfdca4fe45f066d0d81edebb2c102b66d1))
* **types:** add commonjs type declarations ([acb7167](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/acb7167f6794c394b0028e8ac89097c04bd085bd))
* **types:** type the recommended strict configs ([1992b8a](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/1992b8aa8eb0da1770bd992dc58a7ff5d266d4c1))
* update `package.json#description` ([bb5254b](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/bb5254ba26fa4ecda8205ce59ab6ef67548ab9e2))
* when deps is missing, still run rules that don't rely on them ([ec5c7a4](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/ec5c7a4c77a5857bbe2242bc51eb009bee9a74f8))


### Miscellaneous Chores

* manual release ([47d1d60](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/47d1d6068391421583905e68a3e98430136b841d))
* trigger release ([1d07da4](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/1d07da42e9c2af5f27e73ab9ab82f20c0de9dd25))
* trigger release ([83e2af6](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/83e2af64817e0c17def374f839623a94678fd936))


### Code Refactoring

* **no-adjust-some-state-when-a-prop-changes:** remove inaccurate "some" from name ([42d660a](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/42d660ab51cf3cb1f4ccd05bdcd987b26283ce66))
* shorten name of no-adjust-state-when-a-prop-changes and no-reset-all-state-when-a-prop-changes ([584592c](https://github.com/Maveryyoung/eslint-plugin-react-you-might-not-need-an-effect/commit/584592c39c7366c18409c17a0799d800d2b0bbde))

## [1.2.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.1.0...v1.2.0) (2026-11-08)


### Features

* see through TypeScript-only syntax ([4eeb4ad](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/4eeb4ad935e7a426cf2dafbef10d7cbf31f3133c))
* support popular third-party effect wrappers ([2b32a9e](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/2b32a9e005e4fef60b635b62b25c163b51e5a4fb))
* treat context values as props ([8c1c7ec](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/8c1c7ec7015e6ee5a4be28cb5c0f37dc92717619))


### Bug Fixes

* analyze `const Component = function() {}` components ([d26fee7](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/d26fee7d22569884afd07c4fb7e402e8f54ee865))
* analyze effects with omitted or variable deps ([3e7dc7e](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/3e7dc7e3cf8aa4fd25c7c71b13eb852cfbf60b9b))
* don't fall-through to entire enclosing body when `useEffect` fn arg is opaque ([a7039f3](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/a7039f363a069883ca0cd3b02489acc895746f22))
* follow member access on aliases ([0faca35](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/0faca35e082b0a334e62a3d24451a56c790ac5de))
* follow only stable, invoked aliases in call chains ([54c13f6](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/54c13f6d3ba794892ee042f1336a35ef2740030d))
* handle defaults in useState destructuring ([36bda5f](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/36bda5f59d555282c2ed88387c4af07a1824162e))
* ignore non-function effect callbacks ([e6fa03b](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/e6fa03ba1ac5573d0b4d3e00836207d127df1c3a))
* **no-initialize-state:** treat aliased setters in deps as setters ([997216e](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/997216e2d8e68df6460cb55f6f825445d3d0cb06))
* **no-pass-live-state-to-parent:** remove duplicated quotes from message ([96a22c5](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/96a22c58dce13443cc0aa746545a9004a7761b68))
* **no-reset-all-state-on-prop-change:** count useState calls instead of state reads ([23e5bea](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/23e5bea9d275f4e9095629ed240b2c92ae33accd))
* **no-reset-all-state-on-prop-change:** flag when the same setter is called twice ([80a0ec0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/80a0ec0501be38d90df276cbb155bc32fc277b72))
* **no-reset-all-state-on-prop-change:** handle wrapper setters ([493d052](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/493d052fad67f8e60a2940cc8634193345854e13))
* report the written state for wrapper setters ([7bf9dc9](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/7bf9dc9bec0fd729c6e4848c75b5be167bd501e0))

## [1.1.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.0.3...v1.1.0) (2026-11-01)


### Features

* support renamed React hook imports ([a4e0f09](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/a4e0f09c8767ffced39d74ab75abc1fb261b6adb))


### Bug Fixes

* **config:** name the flat configs ([b30550d](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/b30550dabbeebdb023a7a25a603b0650daf643f9))
* **config:** stop adding files to the lint set ([fefa3d1](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/fefa3d1e8002438f05b1288224b54fa9f62dd2e6))
* **no-pass-data-to-parent:** remove duplicated quotes from message ([2b2b42a](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/2b2b42afd1ebbb2b390ebdade3b9251e39530f9c))

## [1.0.3](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.0.2...v1.0.3) (2026-10-30)


### Bug Fixes

* stop defining/recommending browser globals for consumers ([b3ed592](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/b3ed592ef14c7c039451d2a68069b39bf446264b))

## [1.0.2](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.0.1...v1.0.2) (2026-08-20)


### Miscellaneous Chores

* trigger release ([3bbeb2c](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/3bbeb2caadf93f326e6cef6da0a6e968c8e40180))

## [1.0.1](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v1.0.0...v1.0.1) (2026-06-15)


### Bug Fixes

* add `homepage` and `bugs.url` to package.json ([a5395f8](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/a5395f81966b075773babd322bd157af65fbf0d5))
* update `package.json#description` ([02d3f3f](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/02d3f3fd6a9bc4f5472562e8f5d1d7b87be01f81))

## [1.0.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.11.1...v1.0.0) (2026-05-31)

This semantic v1.0.0 release signifies my confidence in the plugin's stability and reliability after many iterations.

Thank you to everyone that contributed real-world issues along the way!

### Miscellaneous Chores

* trigger release ([394a44d](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/394a44d9b66895bad8bc384ed3726f3360798441))

## [0.11.1](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.11.0...v0.11.1) (2026-05-30)


### Features

* add more context to messages for clarity and actionability ([efad9aa](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/efad9aac787c4f906dd4c4445e15baeb77cf9e32))

## [0.11.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.10.4...v0.11.0) (2026-05-29)


### ⚠ BREAKING CHANGES

* **no-external-store-subscription:** new recommended rule

### Features

* **no-external-store-subscription:** new recommended rule ([83267dc](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/83267dcde6315a5a1509a8edf554086e2a75ee20))

## [0.10.4](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.10.3...v0.10.4) (2026-05-29)


### Features

* follow call chains involving aliases ([ddbbb5d](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/ddbbb5d7458ee57dddf054a4eb879ad38b9faf05))
* follow named functions passed to `useEffect`s ([d98285e](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/d98285e166d520aa02e9ac7b4c6982a8ea86cc60))

## [0.10.3](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.10.2...v0.10.3) (2026-05-28)


### Features

* **no-derived-state:** remove `avoidSingleSetter` case ([06a1874](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/06a187427904fac4893ce12563fb0e7841d18dbf))


### Bug Fixes

* ignore arguments to upstream calls when searching for state/props ([b457d15](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/b457d153cd733c35fca14665bb23928302a753d4))

## [0.10.2](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.10.1...v0.10.2) (2026-05-24)


### Bug Fixes

* **no-event-handler:** flag at usage instead of declaration ([bffa6ab](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/bffa6ab27236c59e38fba9235c8d7e165a00e899))

## [0.10.1](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.10.0...v0.10.1) (2026-05-06)


### Features

* more idiomatic recommendation for passing to parent inside custom hooks ([b0dacf4](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/b0dacf4bacbe746c635f6f4efd3134b2a76173f0))
* **no-event-handler:** flag props ([d246668](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/d246668dc8f4f1c34bd9cc134d539992b38e8cb5))


### Bug Fixes

* **no-initialize-state:** analyze effects that only have setter in deps ([1a7174f](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/1a7174fc1296165fecaa8ef518d7b5b5faaecd8e))
* when deps is missing, still run rules that don't rely on them ([cefdfcd](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/cefdfcdbd1c199be0747997b0de3a4ed9476e657))

## [0.10.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.9.3...v0.10.0) (2026-05-02)


### ⚠ BREAKING CHANGES

* **no-empty-effect:** remove rule ([#67](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/issues/67))

### Features

* **no-empty-effect:** remove rule ([#67](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/issues/67)) ([1fbc74a](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/1fbc74a2833a84fee2f388fb37102d346e520d52))

## [0.9.3](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.9.2...v0.9.3) (2026-04-08)

### Refactors

* **build**: use tsdown, add publish validation ([cc2101a](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/cc2101a28ae83d4e11c421bbfaee11ffaa26bcb8))

### Miscellaneous Chores

* manual release ([f01d76d](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/f01d76d7e58460106c431f7d4357065688396709))

## [0.9.2](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.9.1...v0.9.2) (2026-03-03)


### Bug Fixes

* dont consider calls to be prop callbacks when they merely receive a prop arg ([3feb48f](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/3feb48f09e21548ff14de1185418794e2b63392e))

## [0.9.1](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.9.0...v0.9.1) (2026-02-15)


### Bug Fixes

* **types:** type the recommended strict configs ([e65513d](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/e65513df307ab26525f30fb026ceaa5870f6af32))

## [0.9.0](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/compare/v0.8.5...v0.9.0) (2026-02-14)


### ⚠ BREAKING CHANGES

* **no-pass-ref-to-parent:** remove rule

### Features

* **no-pass-ref-to-parent:** remove rule ([8428e47](https://github.com/nickjvandyke/eslint-plugin-react-you-might-not-need-an-effect/commit/8428e477d5d54a24c231f5581c92ee4332a88288))
