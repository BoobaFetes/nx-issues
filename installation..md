npx create-nx-workspace@latest my-app-wksp --pm=yarn --preset=apps  --interactive --no-nxCloud
cd my-app-wksp
yarn add @nx/express @nx/react
yarn nx g @nx/react:application client --tags="client, application" --bundler=webpack --pascalCaseFiles --routing --style="@emotion/styled" --no-strict --e2eTestRunner=none
yarn nx g @nx/express:application server --tags="server, application" --frontendProject client --pascalCaseFiles --unitTestRunner=jest