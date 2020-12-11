# Building Search into your Application Workflow


## <a id="overview"></a>Overview
With the wealth of content offered within the Refinitiv ecosystem, the following series of examples will outline the core capabilities available within Refinitiv's Search API, a powerful, Google-like search engine covering content such as quotes, instruments, organizations, and many other assets that can be programmatically integrated within your business Workflow.

Details and concepts are further explained in the [Building Search into your Application Workflow]() article published on the [Refinitiv Developer Community portal](https://developers.refinitiv.com).

## <a id="disclaimer"></a>Disclaimer
The source code presented in this project has been written by Refinitiv only for the purpose of illustrating the concepts of creating example scenarios using the Refinitiv Data Platform Library for Python.

***Note:** To [ask questions](https://community.developers.refinitiv.com/index.html) and benefit from the learning material, I recommend you to register on the [Refinitiv Developer Community](https://developers.refinitiv.com)*

## <a name="prerequisites"></a>Prerequisites

To execute any workbook, refer to the following:

License(s):

- A Refinitiv desktop license (Refinitiv Eikon or Refinitiv Workspace) that has API access 

  **OR**

- A [Refinitiv Data Platform (RDP)](https://developers.refinitiv.com/refinitiv-data-platform/refinitiv-data-platform-apis) license with access to the [Search endpoint](https://api.refinitiv.com/) data services

[Development Environment](https://developers.refinitiv.com/en/api-catalog/eikon/eikon-data-api/tutorials#setting-up-a-python-development-environment)

- Tested with Python 3.7
- Packages: [rdp](https://pypi.org/project/refinitiv-dataplatform/) [pandas](https://pypi.org/project/pandas/) datetime dateutil
- RDP for Python installation:  '**pip install refinitiv-dataplatform**'

## <a name="setup"></a>Setup

The application package includes a series of Jupyter Notebooks demonstrating features of the service.  Depending where you plan to access the content from, you will need provide the proper credentials:
* **Desktop Access**
  
  The notebooks have been set up and tested to access data within the desktop, whether Refinitiv Workspace or Eikon.  For each, you simply need to replace the **'Your API Key here'** with your own [generated application API key](https://developers.refinitiv.com/en/api-catalog/eikon/eikon-data-api/quick-start#create-app-key).
  
* **Platform Access**
  
  If you have an RDP license, you will need to replace the session code segment at the top of each notebook.  Replace the following line:
  
  ```
  rdp.open_desktop_session('Your API Key here')
  ```
  
  With the following:
  
  ```python
  rdp.open_platform_session(
    "Your API Key here",
      rdp.GrantPassword(
          username = "<YOUR MACHINE ID>",
          password = "<PASSWORD>"
      )
  )
  ```

### <a id="authors"></a>Authors

* **Nick Zincone** - Release 1.0.  *Initial version*



