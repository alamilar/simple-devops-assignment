# DevOps assignment

Please read the whole Readme file before proceeding!

## Summary

Prepare a Jenkins instance with one job which will
- Download CPython source code (main branch will suffice)
- Build it
- Gather and present compiler warnings in Jenkins job
- Archive resulting `python` binary as an artifact
- Measure coverage of the C code, convert results to Cubertura format, and present the report in the Jenkins job (see hints for details)

Keep it simple - don't overcomplicate your solution, use Jenkins as an admin, do not care about security configuration/etc.
Keep in mind that the environment must be

## Desired outcome
- A git repository with your solution. It should contain:
    - Docker-compose and Dockerfile you used to setup the environment
    - Jenkinsfile with pipeline used to complete objectives from the summary
    - The repository mentioned above should be avaliable for review - please post it to GitHub/Bitbucket/similar site. Mail the link to your recruiter as soon as possible. Do not use the fork button - this will make your repository visible to other candidates!
- Ability to have a review of your solution on your PC - do not delete the containers/images/volumes from your PC. Apart from reviewing the files, I'd like to see your solution in action, during a call.

## Hints
- Following articles are your friends :)
- https://devguide.python.org/getting-started/setup-building/#unix
- https://devguide.python.org/testing/coverage/#measuring-coverage-of-c-code-with-gcov-and-lcov
- It seems that you need to run gcovr with following parameters to make it work with CPython code:
  `--merge-mode-functions=separate --gcov-ignore-parse-errors all`
- Yes, you'll need to install additional plugins to get everything working, stick to most popular ones
- Partial solution is better than no solution
- Dockerfile and gcovr parameters were provided to you for your convenience!
- Remember about cleaning the workspace :)

Good luck!
