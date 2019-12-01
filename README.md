# asdf GitHub Actions [![GitHub Workflow Status](https://img.shields.io/github/workflow/status/asdf-vm/actions/test?style=flat-square)](https://github.com/asdf-vm/actions/actions)

This repo provides a collection of asdf related actions for use in your workflows.

## Main actions

These two actions are probaly the most useful:

* `asdf-vm/actions/install@v1` - Install your `.tool-versions` plugins and tools.

  ```yaml
  steps:
    - name: asdf_install
      uses: asdf-vm/actions/install@v1
  ```

  See [action.yml](install/action.yml) inputs.

* `asdf-vm/actions/plugin-test@v1` - Test your shiny new asdf plugin.

  ```yaml
  steps:
    - name: asdf_plugin_test
      uses: asdf-vm/actions/plugin-test@v1
      with:
        command: "my_tool --version"
  ```

  See [action.yml](plugin-test/action.yml) inputs.

## Lower level actions

These actions are used internally by the above ones. And you wont need
to use them directly, unless you actually want ;)

* `asdf-vm/actions/plugins-add@v1` - Only install plugins, not tool versions.

  See [action.yml](plugins-add/action.yml) inputs.

* `asdf-vm/actions/setup@v1` - Just installs asdf itself.

  See [action.yml](setup/action.yml) inputs.
