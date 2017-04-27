# react-playground

## Running

First `npm install` to grab all the necessary dependencies. 

Then run `npm start` and open <localhost:7770> in your browser.

## Production Build

Run `npm build` to create a distro folder and a bundle.js file.

## react-intl-redux

localisation

```sh
use api to translate :

import { intlShape, injectIntl, defineMessages } from "react-intl";

define a message descriptor: 
const messages = defineMessages({
  editDescription: {
    id: "Edit",
    defaultMessage: "Edit"
  },
  deleteDescription: {
    id: "Delete",
    defaultMessage: "Delete"
  }
});

each message descriptor should have properties id and defaultMessage,

then  inject intl to component :

injectIntl(connect(
  mapStateToProps,
  mapDispatchToProps
)(PendingClaimsPage));

call intl.formatMessage(messages.editDescription) to translate text "Edit".

Use React-intl component :
import { FormattedMessage } from "react-intl";

<FormattedMessage {...messages.editDescription} />
```
More usage pls check [this link]("https://github.com/yahoo/react-intl/wiki#getting-started "Title").

### Optional Plugins for Chrome
* [React Dev Tools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en)
* [Redux Dev Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)

## Linters

Linting tools help enforce code standards as we write.
* [ESlint](http://eslint.org) with [React](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/prop-types.md) and [Accessibility](https://github.com/evcohen/eslint-plugin-jsx-a11y#installation) extensions. [Editor integration](http://eslint.org/docs/user-guide/integrations)
* [SCSS Lint](https://github.com/brigade/scss-lint). [Editor integration](https://github.com/brigade/scss-lint#editor-integration)

Config files are available in config. Normally the config file names start with "." and are hidden on MacOS/Unix however they've been renamed without the dot so you can see what's going on.
* Windows: copy scss-lint.yml %userprofile%\scss-lint.yml & copy eslintrc.js ..\..\.eslintrc.js
* Mac/Unix: cp scss-lint.yml $HOME/.scss-lint.yml | cp eslintrc.js ../../.eslintrc.js
