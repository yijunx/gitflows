# gitflows
* just to test some gitflows and see how

    ```
    git checkout -b hotfix/some-fix-001
    # do something commit and push 
    ```

* go to github and merge to main


# before start

* create the repo
* clone
* create and swtich to the dev branch

    ```
    git checkout -b dev
    ```

* write something in the dev branch and commit and push first

# feature branch

* create the feature branch (while at dev)

    ```
    git checkout -b feature/feature-001
    ```

* do some edit, do some commit

    ```
    git add .
    git commit -m "some changes are done on feature branch"
    ```

# back to dev

* dev branch needs to get stuff from feature branches, and hopefuly triggers a build and deploy to DEV env.


    ```
    # switch back to dev
    git checkout dev
    # pull the changes from feature, here there is debate, whether we merge or rebase
    git pull origin feature/feature-001
    # now your local dev has the changes from feature branch, use git push to update dev
    git push
    ```

* above process should be done via a pull request, do direct push to dev should be allowed.

# PR to update the main from dev

* using github frontned, then merge

# now lets say we have another feature...

    and there is a hotfix done ...
    ```
    git checkout -b feature/feature-002
    ```

    get the changes from the hot fix (which merged to main already)

    ```
    git pull origin main
    ```

