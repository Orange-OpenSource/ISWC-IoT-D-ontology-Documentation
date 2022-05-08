# IoT-D ontology
Vocabulary definition for IoT dependencies toward collaborative device management. The vocabulary documentation is built using the [Widoco](https://github.com/dgarijo/Widoco) toolset, forked from [era-vocabulary](https://github.com/julianrojas87/era-vocabulary).
![alt text](https://github.com/Orange-OpenSource/ISWC-IoT-D-ontology-Documentation/blob/master/iotd.svg?raw=true)


For deployement Follow the next steps:

1. Clone this repository:

   ```bash
   git clone https://github.com/Orange-OpenSource/ISWC-IoT-D-ontology-Documentation.git
   ```

2. Normally the latest built version of the Widoco documentation is already available within the repository in the [`public`](https://gitlab.tech.orange/device-management-a-r/recherche/these/these_collaborative_iot_dm/iot-d-ontology-documentation/tree/main/public) folder. If you want to deploy this version then skip to step 4, otherwise proceed to delete all the files and folders in `public/`:

   ```bash
   cd public
   rm -rf *
   ```

   Now continue to the next step.

3. Generate the Widoco documentation:

   ```bash
   ./generate-docs.sh
   ```

   The resulting sources will be placed in the `public/doc` folder.

4. Publish the Web page. In this example we use Node.js's [`npx`](https://nodejs.dev/learn/the-npx-nodejs-package-runner) utility and [`http-server`](https://github.com/http-party/http-server) for this, but you may choose to publish the static files otherwise (e.g. directly via NGINX).

   ```bash
   cd public/doc
   npx http-server --cors -p ${PORT}
   ```

   Replace `${PORT}` for the TCP port where you want to run the application. Once the application is running you may access the following resources:

   - The vocabulary documentation at `http://localhost:${PORT}/index-en.html`.
## License
 
 
 This software is distributed under CC-BY-NC-SA 2.0: https://spdx.org/licenses/CC-BY-NC-SA-2.0.html 

Copyright (c) 2022 Orange

## Dependencies
widoco - jar file

## Contact
 * e-mail: amal.guittoum@orange.com
