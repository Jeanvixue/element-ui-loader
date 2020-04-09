# Brief Introduction
Inspired by iview-loader, uniform element-ui tag writing specification, all tags can be used in the form of capital letters, including two tags Switch that are restricted by Vue.

Although not recommended, you can use the loader option configuration to open all tag prefixes, such as el-form.
# Usage
## Install
First, install element-ui-loader through npm
`npm install element-ui-loader`
## Setting
Configure webpack to rewrite the normal element-ui-loader configuration, such as:
```
module: {
    rules: [
        {
            test: /\.vue$/,
            use: [
                {
                    loader: 'vue-loader',
                    options: {
                        
                    }
                },
                {
                    loader: 'element-ui-loader',
                    options: {
                        prefix: false
                    }
                }
            ]
        }
    ]
}
```
## Illustrate
After the parameter `prefix` is set to `true`, all element-ui component tag names can be prefixed, such as `<el-row>` and `<el-select>`
# License
MIT