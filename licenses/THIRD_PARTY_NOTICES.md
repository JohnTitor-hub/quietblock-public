# Third party notices

Quietblock is distributed under GPL version 3. The full license is in `LICENSE`.

Copyright (C) 2026 Quietblock contributors, for original Quietblock contributions. Upstream components retain their original copyright and license notices below and in their source files.

- `vendor/eyeo-sdk`: eyeo Web Extension Ad-Filtering Solution and Adblock Plus Core, copyright eyeo GmbH and contributors. GPL version 3; see the included `COPYING` files and `LICENSE-THIRD-PARTY`.
- `vendor/eyeo-snippets`: eyeo Anti-Circumvention Snippets, copyright eyeo GmbH and contributors. GPL-3.0-only; see its `COPYING` and `LICENSE.js`.
- The included jsbn implementation retains its original license under `vendor/eyeo-sdk/adblockpluscore/vendor/jsbn/LICENSE`.
- Dependency licenses remain available in their npm packages. Filter list provenance and licenses are recorded with each snapshot.

The production npm components retain their own licenses: Mozilla's `webextension-polyfill` 0.12.0 (MPL-2.0), `rusha` 0.8.14 (MIT), and `uuid` 14.0.3 (MIT). Quietblock bundles/minifies their published code without changing their APIs. Mozilla's preferred source is available at [its corresponding published revision](https://github.com/mozilla/webextension-polyfill/tree/1649d84ad93c6ebb7225a3db44e96c33e6bbb4a7). The matching release-source ZIP also includes the original preferred-source archives and license files for all three under `runtime-dependencies/`. `dependencies-source.lock.json` and the extension's `notices/dependency-source-provenance.json` record their publication versions, source revisions, archive hashes and npm integrity values. Upstream notices remain intact; the source components retain their original licenses.

Filter data retains its own licensing and attribution:

- EasyList and EasyPrivacy are by [the EasyList authors](https://easylist.to/), under the licenses described on their [license page](https://easylist.to/pages/licence.html).
- Fanboy's Annoyance List is by its authors, sourced from `https://easylist-downloads.adblockplus.org/v3/full/fanboy-annoyance.txt`. Its snapshot declares [Creative Commons Attribution 3.0 Unported](https://creativecommons.org/licenses/by/3.0/). The eyeo package's GPL label does not replace that declaration.
- The anti-circumvention snapshot is distributed in the pinned GPL-3.0 eyeo filterlists package; its upstream project and package integrity are recorded in `filters/lock.json`.

Original snapshot headers and text are preserved. Quietblock compiles these lists into Chrome network rules and content-filter data; these generated forms accompany the original snapshots and their attribution in the extension.

`upstream.lock.json` records original repository revisions and archive digests. Git history records Quietblock's modifications to the vendored engine; it is a maintained reduced fork, not a claim of an unmodified upstream distribution.

The complete vendored source, build scripts, dependency lockfile, and filter snapshots accompany the extension source so recipients can reproduce the distributed code.

Distribute each extension ZIP with the source archive for the same release commit, or an equally accessible corresponding source download. Use `npm run release:prepare` to include the project's committed source and the pinned runtime dependency source archives. The README describes this procedure; a plain project-only `git archive` does not add those dependency archives.
