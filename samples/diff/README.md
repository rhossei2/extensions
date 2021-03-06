Diff UI Extensions
-------------

The diff editor extension shows the diff between the draft value and the published value of a short text field.

![Screenshot of Diff extension](http://contentful.github.io/ui-extensions-sdk/assets/diff-extension.png)

### Requirements

- Contentful
    - a space to use the widget and the space id
    - an api key for Contentful's Mangement API
- Local machine
    - npm installed and configured on your system
    - Extensions [CLI tool installed](https://github.com/contentful/contentful-extension-cli)

### Installation

- Clone the repository or download the repo as a [zip](https://github.com/contentful/ui-extensions-sdk/archive/master.zip)
```bash
git clone git@github.com:contentful/ui-extensions-sdk.git
```
- Navigate into diff folder
```bash
cd examples/diff
```
- Create a configuration file with your credentials for Contentful
```bash
touch .env
echo "SPACE_ID={YOUR-SPACE-ID}" >> .env
echo "CONTENTFUL_MANAGEMENT_ACCESS_TOKEN={YOUR-MANAGEMENT-TOKEN}" >> .env
```
and replace space ID and management token accordingly.

Source the file to add the variables to your environment.
```bash
source .env
```
### Upload the extension to Contentful

- Create the extension in your space on Contentful
```bash
npm run create
```

### Update the extension

- Update the extension in your space on Contentful
```bash
npm run update
```

### Local development

- Start a local server (replace your port if needed)
```bash
python -m SimpleHTTPServer 3030
```
- Tell contentful to render the widget from your local machine
```bash
npm run dev
```

### Using the extension in the Contentful App

Next, we will enable the extension in the Contentful App for a “Short text” field so that you can see it in action.

In your space, choose any Content Type with a “Short text” field or create a new one. Then open the “Settings” dialog for a field and switch to the appearance tab. A widget with the name “Wistia video widget” should be visible at the end of the list. (Note that you need to reload the app after you uploaded a widget.) Select the widget from the list and save the Content Type. Finally you can open an entry for that Content Type and see the widget rendered.
