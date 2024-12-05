# Expo Android Build Failure: AaptOptimize Error

This repository demonstrates a common error encountered during the Android build process using Expo CLI. The build fails with the error: `Execution failed for task ':app:processDebugResources'. > A failure occurred while executing com.android.build.gradle.internal.res.AaptOptimize. > Could not read resource: /path/to/your/project/android/app/src/main/res/values/strings.xml`

This usually points to an issue within the `strings.xml` file or a problem with the way Android resources are handled in your project.  The `bug.js` file simulates the problematic code, and `bugSolution.js` provides a solution.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Attempt to build the Android APK using `expo build:android`.  You should observe the error mentioned above.
4. Examine the `bugSolution.js` to observe how the problem can be solved.

## Solution

The solution involves carefully checking the `strings.xml` file for any syntax errors, incorrect XML formatting, or unexpected characters. The common causes are:

* **Invalid XML syntax:**  Missing closing tags, incorrect nesting, or malformed attributes.
* **Encoding Issues:** Incorrect character encoding in `strings.xml`.
* **Conflicting Resource Names:** Duplicate string names within the `strings.xml` file or across different resource files.
* **Special Characters:** Improperly encoded special characters.

By fixing the identified issues in `strings.xml`, the Android build process should complete successfully.