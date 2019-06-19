Step 1: Login and add your authorization code\n  1. Visit [PAN
  support](https://support.paloaltonetworks.com).\n  2. Select the Assets > Site Licenses
  tab.\n  3. Select Add Site License.\n  4. Enter the authorization code.\n  \n Step
  2: Activate the API.\n  1. Select the Enable action in Site Licenses.\n  2. Select
  the API Key link.\n\n  The API key appears onscreen as shown below. Use this API
  key when configuring the integration.\n  For more info on activating the license
  visit - [Activating AutoFocus Licenses](https://docs.paloaltonetworks.com/autofocus/autofocus-admin/get-started-with-autofocus/activate-autofocus-licenses.html)\n\nInstructions
  on building the `query` argument for `autofocus-search-samples` and `autofocus-search-sessions`
  commands:\n   1. Visit [AutoFocus UI](https://autofocus.paloaltonetworks.com/#/samples/global)
  search screen.\n   2. Select the `Advanced...` button on the top right. \n   3.
  Build your query by choosing fields operators and relevant values. You can always
  add an additional condition by \n   selecting the `+` button on the right. On more
  information on how to use the search editor visit - [Work with the Search Editor\n](https://docs.paloaltonetworks.com/autofocus/autofocus-admin/autofocus-search/work-with-the-search-editor.html#id791798e0-2277-41b5-a723-383bd0787816_id597cae40-646e-4a2f-acf5-5fe04d9e2cf0)\n4.
  After building the desired query choose the `>_API` button to open the API syntax.\n5.
  Copy the query value from the `{` and on until the `,\"scope\"` parameter and paste
  it as your `query` argument for both search commands. It should look something like
  this:\n```\n{\"operator\":\"all\",\"children\":[{\"field\":\"sample.malware\",\"operator\":\"is\",\"value\":1},{\"field\":\"sample.create_date\",\"operator\":\"is
  after\",\"value\":[\"2019-06-13\",\"2019-06-13\"]}]}\n``` \n\nImportant note regarding
  `autofocus-sample-anakysis` command: Due to large amount of dynamic outputs, run
  the command once to get the fields and os's under HTTP,Coverage,Behavior,Registry,Files,Processes,Connections,DNS.