# Crane Release Notes: v1.4.0

## Repo: mig-ui

```
fca3f6d Bug 1920664: Add plan level warning conditions (#1114)
ff42bcb add a warn condition for generic warnings on a plan (#1111)
e8dcb2a Add BZ automation to repo (#1108)
4a25b19 Bug fix - Fix small regression with warning condition being hidden on migmigration (#1110)
1ca0bd3 Fix warning condition code for MigMigration selectors (#1105)
422ddfd update oc copy  function to include DIM/DVM resources (#1107)
d9e536d Check for null conditions array when looking for latest rollback (#1103)
2129f8c Bug 1915702: Add check for empty step name when cancelling rollback
894ef9b Handle plan spec overwriting user DIM/DVM  selection when editing (#1093)
043b5a7 Bump ini from 1.3.5 to 1.3.7 (#1088)
a696975 Bump axios from 0.19.2 to 0.21.1 (#1097)
4451188 close bz 1909656 (#1098)
fcc8f8f fix wrong progress bar variant when regex matches resource part of progress string (#1094)
c9d42d5 check location for existing secret instead of assuming openshift-config (#1091)
a2303d7 Allow migrate after rollback (#1090)
30674d5 add check for migration.status.pipeline before setting in selector (#1086)
c9ecced Update storage form to show proper type when editing for azure/gcp (#1083)
c4084f8 Registry pod failure bug (#1082)
9596bf6 Fix for empty ns bug (#1081)
9ee461f Fix an issue with dvm being set to true when not enabled (#1080)
78e26c5 Removes duplicate context and fixes cancel button (#1077)
3bbcf18 fix typo (#1076)
168ba94 DVM Progress (#1073)
7c1de8c remove travis (#1075)
5a5b9d1 add ci file for github actions (#1074)
17bfbc8 Progress updates part 2 (#1072)
4ddf12e fixes app not redirecting when token is expired (#1068)
89a53f4 Disable rollback button after completion, show "Rollback Succeeded" text (#1071)
a86d7dd Add rollback button and info modal, change migration modal to ask positive quiesce question (#1065)
7539140 fix cell widths to prevent flicker when updating (#1061)
faf6753 Fix direct migration bug (#1060)
584badf MIG-119 : Drill down page for migration steps (#1059)
0937290 Add support for direct migrations (#1058)
f869805 Move migrations table/Integrate pipeline (#1053)
5498f73 Move namespaces table (#1042)
c73a823 move to dayjs from moment (#1056)
f4e6258 Fix copy oc command for resources in debug dropdown (#1050)
```

## Repo: mig-controller

```
fa27dd31 Bug 1920911: Do not include DVM volumes in stage backups (#936) (#937)
a7eedda6 Bug 1907828: Adding pvc health checking when pod is pending (#932) (#933)
7877a0e1 Bug 1920548: Adding information on how to debug failure (#920) (#926)
4ff55eb3 Bug 1920683: Turn off munge symlinks to preerve symlinks (#925) (#930)
72891138 Bug 1920678: Removing fake super option as it hides the permissions in extended attributes (#923) (#929)
28d5e8f2 Bug 1920664: if no status is updated by the router, mark the route not admitted (#921) (#927)
1b060813 adding github actions for automation (#904) (#907)
1c31c6ab Bug 1919366: Using non-root rsyncd conf for direct volume migration (#913) (#914)
821a1f0d Bug 1918503 - Prevent panic if migmigration object is deleted while DVM runs (#903)
a830f7be Use Unwrap for api errors that were being checked away from point of creation (#902) (#905)
9ae55878 Bug 1912246 - Add checksum flag to rsync when verify is specified (#890)
3a045e51 Bug 1908270: Add namespace length validation and subdomain override (#897)
dcb3e46a use anyuid unless explicitly requested privileged SCC (#896)
a0a45043 Bug 1915699: Fix client used to get correlation labels for "DeleteCorrelatedRestores" (#898)
12152627 match Rsync Daemon and Stunnel configurations with pvc-migrate (#894)
07f085c3 Cleanup Direct migration Resources when the Cancel operation is invoked (#884)
fd769734 Bug 1907828: Adding claim health checking for a waiting to be created pod (#889) (#895)
de967a67 Revert "Update DVM PVC check to include determination whether PVCs are bound and usable (#852)" (#892)
bbf273d3 make the dvmp name unique for a dvm CR and a vol and ns (#891)
bae18247 Add Validation for Exposed Registry Route (#867)
10d1403d BUG 1908214: carry fsGroup/supp-group id if there are pods running mounted on a pvc (#885)
74589ecc Update DVM PVC check to include determination whether PVCs are bound and usable (#852)
830deb94 Checking desired number of objects before returning "True" in phases (#882)
92094f54 only get registry annotations if it has imagestreams (#887)
ce013eb2 Bug 1908270 - Change DVM route name to 3 characters (#886)
f7cd8bc2 Don't do direct migration when disabled; no registry if disabled
d03fe543 read the pod configurations from configmap (#870)
54778b75 Add a "migrationcontroller" label bsl/vsl to identify controller
e3d6bcf9 bz-1914118 checking for current migration UID for resources while labeling
6df27055 warn a user if dvm controller is blocked because of dependency pods (#868)
2b86f2ec Bug 1913977: add validation for user provided Rsync options (#878)
f669d75d Bug 1906724: Delete moved NFS PVs during rollback (#879)
b89654d0 allow reading Rsync options through environment variables (#874)
0c483a32 Add direct migration resources to debug view (#866)
cd6e11b4 Bug 1910353 - Do not run DVM for snapshot volumes (#873)
6f78df0e Bug 1910518 - Use cluster specific client for transfer image (#871)
949acf82 Update DVM phase descriptions (#850)
cd1f6730 Apply appropriate labels on PVCs to facilitate DVM rollback (#859)
38e1a9d7 Bug 1906810: Failing migration if registry pods are in ImagePullBackOff state (#860)
ebf1dc75 updated warning message for dvm failure (#862)
aa0ca152 Bug 1907785 - Support configurable rsync transfer image (#861)
d766b21d progress reporting for Direct Image Migration
5aecd264 update CamRole to MtcRole (#858)
939da21b Allow another final migration after successful rollback (#851)
cc9971f6 fixed CRD for migmigration to make sure pipeline step started/completed appear (#856)
c1d52710 Schedule Rsync client pods on the same nodes as the volumes (#845)
17ceb172 Create secret to hold rsync password and read from it (#836)
483cd9e8 Fix go mod builds (#854)
d02e8faf fixing CRD condition generation such that conditions can be empty (#853)
b6b83838 remove old CRD's and regenerate (#849)
36968273 Add namespace to `make use-local-controller` (#848)
b5cc9736 Switching mig-controller to go mod (#753)
a5e36093 fix dvm failure warning (#833)
6f9b997f change the deletion policy to `DeletePropagationBackground` (#832)
c25de6b8 Fix DVM resource creation to proper client (#826)
ff4ed4f1 add progress statistics to failed Velero entities (#817)
cdb739f0 Add cleanup phase to DVM controller task start (#819)
a33f77e0 Add status.phaseDescription to DVM CR (#808)
3c2b6f2b add dvm progress information to migmigration (#799)
8840dfb6 Split cleanup into multiple steps for more granular UI view (#814)
0879a7b3 add ability to mark a step skipped (#816)
4e103fd6 update warning messages (#809)
49addd20 [MIG-119] Add: Requeue to Annotation/Label phase (#762)
bc8d59db For direct image migration, skip images on stage backup
8949e3c4 Warn instead of failing migmigration if DirectImageMigration has errors
f33d3bb4 add progress reporting instructios (#793)
68ae2c41 Fix stage itinerary flags from DVM merge (#803)
3a7af4e1 fix StageItinerary after a bad merge conflict selection (#802)
7de05d85 Use ubi8/go-toolset:1.14.7 to avoid ratelimit build failures (#798)
a07a7e0e Bug 1894822: Fix flipped src/dest pods (#797)
0c7cf948 address feedback on PR review:
9445f63b Bubble up progress report to dvm from dvmp (#787)
b92415f8 updating vendor/ to get debug log changes for copyimage (#774)
4312ed1d Strip https:// (or other prefix) from registry path (#777)
7b33feaa Integrate DVM controller into migmigration workflow (#756)
3e335d91 Direct Image Migration migmigration integration (#763)
cefe12a3 CRD and new phases for direct image/volume migration integration
7dd80393 Update HACKING.md
e527abe5 Exit miganalytic reconcile if analytics gathered (#792)
2765575b Remove clusterregistry from scheme (#778)
8ccfb7e9 Remove tracking issue tempate (#779)
c255ed5e Filter velero pod list on currently-running (non-terminating) pods
c24733ee Update descripton.go with stale CR removal phase descriptions (#770)
8d0c914d Default to FastReQ unless PollReQ is more appropriate in task.go (#776)
eca76f1a add failure/stalling scenarios doc for the community (#767)
2bbc2793 Unquiesce apps on destination after final restore (#773)
baca68a3 fix incomplete steps when migration fails/cancels, rename final step to CleanUp (#772)
27fc7fe8 Bug 1871059: Adding ability to wait for init containers to start and finish (#747)
b20990b6 Bug 1882409: Hook job and pod should get purged when migration is cancelled. (#768)
3042340b MIG-119: Backup progress improvements (#764)
eec8dcb8 MIG-351: let the migration run to completion on partial velero restore failure (#760)
32176d29 [MIG-249] Add pre-migration velero CR cleanup + velero restart if needed (#743)
426be0be MIG-323 - Add logging improvements to migplan_controller (#736)
5045918f MIG-323 - Add logging improvements to migmigration_controller (#742)
f8a36fd7 Start quietly when mig-ui is not deployed (#766)
dd58324d MIG-323 - Add logging improvements to mighook_controller (#746)
d4f34c2a MIG-323 - Add logging improvements to miganalytic_controller  (#745)
52a10d7a Refine getRegistryPods query to fetch only the associated registry pods (#752)
ad775f32 Fix PodVolumeBackup & PodVolumeRestore not updating in the discovery inventory correctly. fixes #724
5eeba0a6 fixups: fix typo in arguments (#757)
810faf74 Enhance Makefile to allow for easier running of local controller + discovery (#754)
d2f8c9a0 remove backup replication check (#755)
b09efb29 Update rollback with unquiesce step being run always (#758)
f1d1d198 MIG-284: add phase 1 progress reporting to dvm controller (#734)
c1745a5e Update makefile to use proper build tags for make run (#751)
89c1d242 Fix crash due to missing registry container status (#749)
9b43c97c [Mig-119] Hooks stage progress (#739)
e25ab73a add BUILDTAGS to Makefile (#744)
5733c65e First phase work for direct image migration controller
ce38601e new vendor deps for direct image migration
e530dc77 Only refresh MigPlan from StartRefresh phase (#741)
8d14f830 MIG-119 - Backup/Restore progress reporting (#692)
ff75fba7 [MIG-249] Change stage pod cleanup to remove all stale stage pods from migration namespaces (#738)
12f220fa minor logging changes migstorage (#735)
a9dbfc16 Fix orphaned stage pods (#719)
71ce18ae Add pipeline fields to migmigration CRD (#737)
9284b391 MIG-323 - Add logging improvements to migcluster_controller (#731)
3fa56d66 MIG-119 - Introduce migration pipeline (#706)
57df4eb9 MIG-284 - Phase 1 implementation of direct PVC migration (#711)
30cde46e add log improvements and kube events for status conditions to migstorage (#698)
055770ee Fix discovery debug tree filtering on PVBs/PVRs (#723)
0dcd0b4f MIG-360 - Registry lazy start (#717)
2537a3bc Remove destination stage pod check (#718)
368f456b update without failing due to ClusterIP conflict and fix e2e test suite (#715)
505889a9 Improve mig registry health check by failing fast (#712)
a3aa1b4e update stage pod running check and add destination stage pod check (#675)
fb3ec1b2 Don't count resources that won't be migrated (#676)
9506375b Update migration to support rollback on demand (#677)
115aaf53 Remove all remote watches (#651)
b7a4d4d3 Add StorageClasses to discovery service (#705)
6c28e299 Fix util typo in devguide (#697)
```

## Repo: mig-operator

```
efa0fe3 Add BZ automation to repo (#563)
93cb679 add imagestreamtags to excluded resources when disable_image_migration is set (#565)
42a791a Bug 1912246: Add checksum to dvm CR (#553)
6cf2b38 Bug 1908270 - Include ability to supply custom route subdomain (#552)
939abba MIG-505: add privileged flag for rsync pods (#551)
a39985f Fix 1.4.0 restic restore helper tag (#549)
0b4dcf9 change variable names for rsync client, transfer pods (#543)
0b52474 Add operator.yml and controller-3.yml to root of operator image (#537)
5a9ffcd add rsync option environment variables to mtc controller (#540)
3884965 config map data to configure rsync client, transfer and stunnel pods (#533)
87e2e3f Add rsync-transfer to v1.4.0 operator.yml (#534)
0a072cf Add rsync-transfer to related images (#532)
18d61fc Bug 1907785 - Support configurable rsync transfer image (#531)
ce2689e fix file name in crd task (#529)
dc1399b CRD changes to add DIM progress reporting (#526)
49cd8f7 Update controller name and role (#528)
fe49808 Revert "Update controller name and role"
d49ad5c Update controller name and role
6d0221f remove new doc lines (#527)
6a3827d fixed CRD for migmigration to make sure step started/completed appear (#525)
f6dc663 Feature/mod switch test (#518)
69391a1 remove duplicate dvm entry (#514)
b87ea25 Add log reader to downstream prep (#512)
f97829c add dvm and dvmp to owned CR and fix typo (#509)
f0de496 Update velero CRDS to skip validation <3.11 (#506)
af59558 Test fixes (#504)
61d25ee Update values for 1.4.0 (#502)
2a601be add skipped field to migmigration status (#501)
590cb2f Add mig-log-reader to mig-operator (#500)
ab1903b Add node selector if defined in MigrationController CR (#498)
64dd2c5 update velero CRDs for 1.5.2 (#499)
7fd13d6 CRD changes for direct image/volume migration integration (#489)
f0c0480 add events RBAC for logging change in mig-controller (#491)
76ea264 MIG-284: add DirectVolumeMigrationProgress CR for mig-controller (#484)
f999647 Fix OCP 4.1-4.5 instructions (#490)
64342fb Remove requirement for podman (#488)
43f6d7f Add 1.3.2 skips, add missing files, update release process (#479)
395f68f fix hacking guide (#483)
fa698d9 add route.openshift.io to clusterrole (#485)
e1b3580 add new CRDs for direct image migration (#478)
a208aef fix typo in DVM defn (#482)
978d4f1 Direct volume migration RBAC+CRD additions (#477)
a8e418e add pipeline field to migmigration status (#481)
```

## Repo: velero

```
cd2b18d6 Add BZ automation to repo (#82)
3f93eb9a Vendor code and rebase log for 1.5.2
16a4e473 version bump to 1.5.2
e7203e96 Dockerfile mod=vendor
6fd41015 CVE-1869801 update aws-sdk-go to 1.34.11
91be94df Added support for restic --verify flag
c8bf86c4 Pass s3 BSL insecureSkipTLSVerify flag through to Restic
3668a21e Add support for restic skip-unchanged
f26ea41e Add UBI Dockerfiles for Konveyor
456eb196 Changelogs for v1.5.2
bd6a4d49 Fix version cmd getting nil pointer (#2996)
9675748c Fix BSL controller to avoid invoking init() on all BSLs regardless of ValidationFrequency (#2992)
02cba196 create CRB with velero-<namespace> (#2886)
89fb9028 restore proper lowercase/plural CRD resource (#2949)
845d7ea5 Ensure PVs and PVCs remain bound when doing a restore (#3007)
87d86a45 Add changelog and docs for v1.5 release (#2941)
6e20eaab Spruce up release instructions and release scripts (#2931)
afa552ca Fix url (#2933)
6f374b57 Documentation for maintainers (#2932)
062a598d Update upgrading instructions to right version (#2930)
cfc46510 🏃‍♂️ add shortnames for CRDs (#2911)
d85d785c Remove "exec restore hooks coming soon" line (#2929)
5caa97f3 📖  Fixing typos and markdown formatting (#2917)
6d729a90 🐛 fix 1.5 upgrade insturctions (#2926)
e53369d5 Document exec restore hooks (#2896)
b60e6ff2 v1.5.0-rc.1 release (#2921)
54367814 Update links to point to main branch (#2915)
69611736 Add Bridget to list of maintainers (#2916)
44306e53 📖 add restore hooks doc (#2862)
cd31141b Show format version on velero backup describe (#2901)
0547b1d9 Restore hooks exec (#2804)
a179ae01 Fix for docs redirects (#2895)
be1cd030 Refactor BSL related code (#2870)
b5edac3c 📖 update restore api types with init container restorehooks (#2855)
debcbd2f fix: rename the PV if VolumeSnapshotter has modified the PV name (#2835)
c952932f Migrate ServerStatusRequest controller and resource to kubebuilder (#2838)
aed504a0 Fix git commands and add dry run mode as default to the tag-release.sh script. (#2875)
15136745 fix EnableAPIGroupersions output log format (#2882)
97648455 Add CII Best Practices badge to README (#2880)
1dcaa1bf Rename security policy file to show up accurately in the GitHub UI (#2879)
ac50b457 add hugo default TOC (#2866)
9cf35d9b add new table shortcode (#2865)
36a4c28f point contributors to style guide (#2872)
474de24d 📖 update documentation to push container images using docker buildx (#2854)
648582c8 Update release checklist to include more info around blog posts and r… (#2837)
839a9646 update docs to match style guide (#2861)
7369e4d9 Check for errors on restic backup command (#2863)
03bd6c85 Better var names (#2848)
f5d10c54 Merge pull request #2853 from ashish-amarnath/fix-server-version
20ac6037 🐛 fix passing LDFLAGS across build stages
45168087 v1.5.0-beta.1 changelog and docs (#2849)
97c14e34 Merge pull request #2844 from ashish-amarnath/1.5-upgrade-instructions
718a94ad Invoke DeleteItemActions on backup deletion (#2815)
89d4e441 📖 document velero v1.5 upgrade instructions
71fd7cc5 add index files to api types folder (#2839)
d33982b8 🏃‍♂️remove go mod download from Dockerfile for build speedup (#2842)
e0098d8a Update the number of reviewers for PRs/add Bridget (#2843)
e9ece0f7 Implement DeleteItemAction plugin support (#2808)
d1a1d063 Create Velero security policy (#2797)
e6eb5372 update image link in readme (#2827)
62b2a0e1 The EnableCSI flag on velero backup describe command only (#2817)
9ed43f96 📖 update default-volumes-to-restic exclusion list (#2828)
52b68380 docs: add metadata to resource-filtering.md (#2832)
5d2c9e2b Override logrus.ErrorKey when json logging is enabled (#2830)
3a4e441a add kindfor func to get apiresource from gvk (#2764)
c663ce15 Hugo migration (#2720)
68112359 Checkout code on builder image workflow (#2816)
14170b52 Enhance Backup to backup resources in specific order. (#2724)
dd2d040f Create restore-hooks_product-requirements.md (#2699)
d4bbd7b8 🐛  Patch generated yaml for restore CRD as a hacky workaround (#2814)
827d5d34 Improve and clarify cmd help documentation, flags, and examples (#2736)
98a09bcb add note about windows support (#2806)
9eca0fcb Pass default-volumes-to-restic flag from create schedule to backup (#2776)
70e93912 Add design doc for DeletionAction plugins (#2713)
d7d6a85e Add an auto-rebase workflow (#2813)
7914138d Merge pull request #2802 from ashish-amarnath/fix-restic-restore
e391e431 🐛 Supply command to run restic-wait init container
5b28d70e Switch event to use pull_request_target (#2807)
a68e5fc3 🏃‍♂️ Setup crd validation github action on k8s versions (#2805)
5d6da651 ✨ Implement restore hooks injecting init containers into pod spec (#2787)
9b9bb629 🐛 Make init and exec restore hooks as omitempty in restore hookSpec (#2793)
4364a813 update docs to include cpu/memory defaults for restic (#2772)
6edf279b Merge pull request #2803 from vmware-tanzu/dependabot/bundler/site/kramdown-2.3.0
1386a856 Bump kramdown from 2.2.1 to 2.3.0 in /site
0b87fbbd Update minio.md (#2799)
4e2f4bb6 Add resource filtering page (#2771)
0e8a7a23 always use groupResource.String() when logging (fixes #2795) (#2796)
19e65689 Add the ability to set the allowPrivilegeEscalation property on the Restic restore helper via plugin ConfigMap (#2792)
6ac0398c Reverting change on 1.4 docs and re-applying to main docs (#2791)
db139cf0 Refactor image builds to use buildx for multi arch image building (#2754)
4e05e81c Merge pull request #2786 from skriss/upd-build-badge
c5a21375 update CI badge on README
1fdb647c Add cacert flag for velero backup-location create (#2778)
9de644f1 Add types to implement restore hooks (#2761)
5bafa9b3 Add JenTing Hsiao (#2768)
fcf7f279 Moved FAQ (#2769)
028818a0 exclude vols mounting secrets and configmaps from defaultVolumesToRestic (#2762)
94872ea2 Add github token so action can actually auth (#2766)
8e672408 📖 update VSC DeletionPolicy docs to be inline with code (#2765)
7005879f Fix YAML in auto-assign GitHub Action (#2759)
bc25e789 Add constants for restore hook annotation keys (#2750)
cffb6393 Auto-assign github PR reviewers and assignee (#2758)
9011b192 Add hooks fields to restore context (#2755)
bbcbde08 Create hook package (#2734)
e83ec79d Merge pull request #2751 from ashish-amarnath/fix-boilerplate
2636730e fix copyright year
86efd157 add support for setting SecurityContext (user, group) for restic restore (#2621)
91ccc4ad Add metrics for restic back up operation (#2719)
a63a82fc 📖 update csi docs to document volumesnapshotclass label (#2741)
d0d143e1 Add StartTimestamp and CompletionTimestamp in Restore Status (#2748)
c27c3cd5 Fix path + add helpful message (#2740)
84dbd133 Move style guide to main (#2735)
caeb4ae4 Update changelogs for v1.4.2 (#2705)
e60d9f28 Remove unneeded auto-generated files (#2732)
01e2dcb3 StorageGrid compatibility  (#2712)
9189cffb Design proposal for Restore hooks (#2465)
f42c63af Address insensitive language (#2677)
2376b697 Fix brew-update script, their commands changed (#2711)
eff358e2 replace -q with -f for docker rmi in build-image make target (#2716)
243ac62e Add backupValidationFailureTotal to metrics (#2714)
a368370b k8s 1.18 import (#2651)
9366fab9 Don't check non-code labeled PRs for changelogs (#2710)
13e1eeab Return early from a BSL controller (#2709)
3239b3e9 Design: Backup Resources of Specific Type by Specified Order (#2627)
dbd0aa49 Add a BSL controller to handle validation + update BSL status phase (#2674)
3d3b9e31 Revert "🐛 fix file perissions on the manifest JSON in backup archive (#2685)" (#2700)
a0d2fc2f Clarify migration between cloud providers (#2666)
54aa75a4 Adjust restic timeout and pod values up (#2696)
c8f4b60b Add scripts for tagging Velero releases (#2592)
695715ff Fix missing quotes that are breaking page render (#2698)
841d6498 Merge pull request #2667 from ashish-amarnath/link-blog
0a53aeeb 📖 make external blogposts clickable links
dae5230a 🐛 fix file perissions on the manifest JSON in backup archive (#2685)
4c76fc9f add style guide file (#2619)
c3cac0a9 design: progress on backup/restore operations by volume snapshotters (#2543)
b4465e92 🐛 Use CRD version prior to remap_crd_version backup item action (#2683)
2d48ac79 Image handling (#2620)
e6130890 Merge pull request #2661 from carlisia/c-skriss
94a9522f updated acceptable values on cron schedule for day of the week from 0-7 to 0-6 (#2676)
b9688130 Add linter (#2615)
4048c020 Convert manifests + BSL api client to kubebuilder (#2561)
6e86a83c Add RBAC page to table of contents (#2659)
0b8e2cbb Improve velero download doc (#2660)
f4cc7cd4 Change maintainer
fcf0f3e5 move csi pluing out of prototype (#2636)
7b1126ff Merge pull request #2655 from carlisia/c-header
ae1f4e28 Merge pull request #2611 from ashish-amarnath/restic-by-default
a191363e Add header info + fix broken tags
e5e7c025 fix copyright boilerplate
7abd2c6d doc updates
af79f965 Merge pull request #2638 from adamrushuk/update-docs
c58331d4 add a supported provider: Storj object storage (#2635)
043c628f remove skriss as maintainer, add nrb as tech lead (#2642)
e9820b98 Merge pull request #2640 from ashish-amarnath/allow-changelog-ignore
c8c2e710 Merge pull request #2641 from ashish-amarnath/reorg-build
43305ec7 🏃‍♂️allow ignoring missing changelog
5ad7a554 Merge pull request #2639 from ashish-amarnath/rogue-br
a7e9fbaf 🏃‍♂️ pass git state to build from makefile
3c94b36b 🏃‍♂️ remove stray html tags
2af9d6a5 Changed pr number for changelog
e7b413c7 Update basic-install and release-instructions documentation for Windows Chocolatey package
6a8dca6b add default-volumes-to-restic flag to velero installation
63f7690f more tests
0bdd6ef5 Merge pull request #2629 from adamrushuk/master
0daea437 Merge pull request #2625 from tbatard/jekyll-to-hugo-migration
6a895be4 add windows cli installation option via chocolatey for docs v1.4
b0fd3d35 rename field
b7117322 add velero server flag to allow default restic use on all pod volumes
dd11b175 changelog
8a2a852b use backup's defaultRestic flag to identify pod volumes using restic
f34aab25 add default restic flag to backup create cli
69cceb0d add backup level flag to opt-in for default restic use
c29a3a4e Merge pull request #2624 from vmware-tanzu/michmike-patch-1
d1b18842 changed pr number for changelog
a728ea80 add windows cli installation option via chocolatey
9518ac89 Add changelog
07da583e Update Jekyll to 4.1.0
30051e67 Update ROADMAP.md
a5346c1a azure: support aad-pod-identity auth when using restic (#2602)
13afbf39 Merge pull request #2613 from ashish-amarnath/changelog-check
e1eba6f4 changelog
5643b0f6 add a CI check for changelog file
d9d9dc60 Log when a hook timeout duration can't be parsed (#2610)
1c80ba90 don't error during backup when additional items returned by plugin don't exist (#2595)
2fd9d900 Merge pull request #2608 from skriss/vsphere-support
305732b3 docs: move vSphere plugin into velero-supported section
ac2905b4 creating the Velero ROADMAP.md (#2548)
7ca08730 Add emoji support (#2594)
0f934bc4 updating governance for Velero - WIP (#2541)
eaec20f2 Merge pull request #2553 from ashish-amarnath/csi-blog
1de95567 blogpost announcing CSI snapshotting capability
e7b668af Merge pull request #2588 from ashish-amarnath/remove-travis
be48119c update release instructions
6aecc0f6 remove travis config
86878063 update build status badge on readme
ceae7a2f When creating backup from schedule, allow default name (#2569)
40d8511f Add status column to get BSL output (#2493)
93612087 Merge pull request #2584 from ashish-amarnath/github-actions
941b804a setup ci in github actions
5b52fd3e re-instantiate backup store just before persisting artifacts (#2550)
d10eea3b Add up and down votes to the issue templates and contributing guide (#2583)
759da5b5 Add instructions for bumping homebrew version (#2580)
c283e62d Merge pull request #2578 from a-mccarthy/v1.4-blog
cbd0ba53 fixing post image and blog date
95e815f2 Update site/index.html
3384da19 adding 1.14 blog post
```

## Repo: openshift-velero-plugin

```
2e1cfe4 Bug 1923722: Disable image tag restore plugin (#70)
2c557f4 Add BZ automation to repo (#68)
9eb2d95 Bug 1906730 - annotate PV with previous reclaim policy (#67)
8f1af0f Fix pod restore plugin (#66)
05c5806 Bug 1892239 - Wait for secrets to be created before restoring pods (#65)
335ab7b Return dependent (#57)
30e45cf change manifest log output to debug (#64)
4226a7a Skip image copy if outside of OADP/CAM (#61)
f5883b4 refactored imagestream image copy into package for reuse (#62)
535ab0b Add restored objects labels (#58)
```

## Repo: velero-plugin-for-microsoft-azure

**NO CHANGES**

## Repo: velero-plugin-for-aws

**NO CHANGES**

## Repo: velero-plugin-for-gcp

**NO CHANGES**

## Repo: restic

**NO CHANGES**

## Repo: hook-runner

**NO CHANGES**

## Repo: must-gather

```
cd5e0ae Carry over changes to add additional resources in directory structure (#23)
cdf34d0 Add BZ automation to repo (#21)
171df03 Bug 1898522/1897501: Update Makefile to launch prom v2.21.0 to match OCP 4.6, fix wal mount dir (#16)
```
