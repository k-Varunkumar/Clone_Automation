## Creating a Automated clone snap-in
So whenever a workitem a clone of that workitem is created, drawback using automation event trigger for work_created is that the clone created iin itself is a new workitem so a clone of that clone is created and this keep on going.
### Steps to create Automated clone snap-in
1. Most of the steps are same as we did for Helloworld snap-in
2. In .yaml file we create a function and define in automation function
3. now every time a workitem is created, the function defined is executed
4. We can also run this locally since, for every function, a json file for input for that function is present in the template, so we can test our function against that input
5. So this can be executed using following command in ./code
```
npm run start:watch -- --functionName=function_1 --fixturePath=function_1_event.json
```
6.now nodemon is activated, and for every save that we do it is tested against the input .json file\
7.once this is done same thing is repeated as in helloworld snap-in,npm install,run build, run package, create package,create version\
8.so once we install this in our snap-in UI, we can install it and after this, for every workitem created, no. of clones are created and stopped only when we disable this snap-in from the UI
