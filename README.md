
### Setup Node Environment

You'll need to create a new node server. Open a new terminal within the project directory and run:

1. Initialize a new project: `npm i`
2. run the development server with `npm run dev`
3. create Archive.zip with `npm run build`

### Create a new endpoint in the server.ts file

The starter code has a task for you to complete an endpoint in `./src/server.ts` which uses query parameter to download an image from a public URL, filter the image, and return the result.

We've included a few helper functions to handle some of these concepts and we're importing it for you at the top of the `./src/server.ts`  file.

```typescript
import {filterImageFromURL, deleteLocalFiles} from './util/util';
```

### Deploying your system

1. Follow the process described in the course to `eb init` a new application 
2. `eb create` a new environment to deploy your image-filter service! 
3. make sure that below file contains deploy section as below contains 
```
deploy:
  artifact: ./www/Archive.zip
```

```
root@vm:~/image-filter-application# cat .elasticbeanstalk/config.yml

branch-defaults:
  master:
    environment: new-app-dev
    group_suffix: null
deploy:
  artifact: ./www/Archive.zip
global:
  application_name: new-app
  branch: null
  default_ec2_keyname: bishoy-udacity
  default_platform: Node.js 16 running on 64bit Amazon Linux 2
  default_region: us-east-1
  include_git_submodules: true
  instance_profile: null
  platform_name: null
  platform_version: null
  profile: eb-cli
  repository: null
  sc: git
  workspace_type: Application

```
4. Don't forget you can use `eb deploy` to push changes.

## Output

Endpoint link
