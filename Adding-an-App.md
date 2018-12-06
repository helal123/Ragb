If you want to add an app that is not currently supported, here is how you go about that:
1. Fork the [UserLAnd-Assets-Support](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support) repository.
2. The list of apps supported is controlled by the [apps.txt](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support/blob/staging/apps/apps.txt) file..
3. The header in that file, describes what each field means, but there are some things that would be good to point out.
   * If the app `Category` is `Distribution`, the `App Name` and `Filesystem Type Required` must match.
   * If the app `Category` is not `Distribution`, the `Filesystem Type Required` must be `debian` (for now).
   * `isPaidApp` must be `false`.
   * We currently don't look at `version`.
4. Each app must have a subdirectory matching the `App Name` created for it [here](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support/tree/staging/apps).
5. That subdirectory must have a `.sh` a `.png` and a `.txt` file with the name matching `App Name`.
6. The `.png` should be relatively small, like 256x256, and ideally look nice and be transparent around the icon.
7. The `.txt` should have a brief description of what the app is.  Currently this does not support localization, so these are all in English (sorry, we will figure this out later).
8. The `.sh` does everything needed to setup and run the app.  Here is a really [simple example](https://github.com/CypherpunkArmory/UserLAnd-Assets-Support/blob/staging/apps/adventure/adventure.sh).  Note, these scripts always start by deleting themselves.  We copy them into profile.d and have them delete themselves so they only run once.  

If you are creating a new distribution, you have more work to do.  Read about that [here](https://github.com/CypherpunkArmory/UserLAnd/wiki/Adding-a-Distribution).


