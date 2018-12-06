If you want to add an app that is not currently supported, here is how you go about that:
1. The list of apps supported is controlled by the [apps.txt](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support/blob/staging/apps/apps.txt) file found in the [UserLAnd-Assets-Support](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support) repository.
2. The header in that file, describes what each field means, but there are some things that would be good to point out.
   * If the app `Category` is `Distribution`, the `App Name` and `Filesystem Type Required` must match.
   * If the app `Category` is not `Distribution`, the `Filesystem Type Required` must be `debian` (for now).
   * `isPaidApp` must be `false`.
   * We currently don't look at `version`.
3. Each app must have a subdirectory matching the `App Name` created for it [here](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support/tree/staging/apps).
4. That subdirectory must have a `.sh` a `.png` and a `.txt` file with the name matching `App Name`.

