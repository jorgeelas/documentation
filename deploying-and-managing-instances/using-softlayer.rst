Using SoftLayer
********************************

Automate application deployments through ElasticBox when you launch to Linux or Windows virtual servers in the IBM SoftLayer public cloud. ElasticBox simplifies deployments with a dedicated focus on applications rather than infrastructure. See the `benefits and use cases </../documentation/>`_.

**In this article:**

* `Register SoftLayer provider in ElasticBox`_
* `Deploy to SoftLayer from ElasticBox`_

Register SoftLayer Provider in ElasticBox
---------------------------------------------

You need a `SoftLayer account <http://www.softlayer.com/info/free-cloud>`_ to be able to deploy from ElasticBox. When you have an account, follow these steps to register it in ElasticBox to automate your deployments.

**Steps**

1. Log in to the `SoftLayer portal <https://control.softlayer.com>`_.
2. Under Account > Users > API Key, click **Generate** to create an API Key or click **View** to copy it. ElasticBox needs the key to make API requests on your behalf.

	.. raw:: html

		<div class="doc-image padding-1x">
			<div class="browser-feature">
				<div class="indicators">
					<div class="circle magenta"></div>
					<div class="circle orange"></div>
					<div class="circle green"></div>
				</div>
				<div class="browser-window">
					<img class="img-responsive" src="/../assets/img/docs/providers/softlayer-getapikey.png" alt="Find the API Key in Your SoftLayer Account">
				</div>
			</div>
		</div>

3. Copy the API key.

4. In ElasticBox, go to Providers > New Provider and select **SoftLayer**.

5. Enter the SoftLayer username and API Key as shown and save.

	.. raw:: html

		<div class="doc-image padding-1x">
	    	<img class="img-responsive" src="/../assets/img/docs/providers/softlayer-entercredentials.png" alt="Enter SoftLayer Credentials">
	    </div>

Deploy to SoftLayer from ElasticBox
--------------------------------------

Select from the following deployment profile options to launch workloads on Linux or Windows machines.

Note a couple of things about instances you deploy on SoftLayer through ElasticBox.

* Tags. You can apply up to six provider tags on any instance you deploy on SoftLayer if you've `defined the tags </../documentation/managing-your-organization/resource-tags/>`_ in the ElasticBox admin console.
* Instance name. Depending on the number of instances you spin up through ElasticBox, each instance is assigned a name that has the format of service_ID-instance_number.domain.com.

**Deployment**

+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Option                           | Description                                                                                                                |
+==================================+============================================================================================================================+
| Provider                         | Select a SoftLayer account registered in ElasticBox.                                                                       |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+

**Resource**

+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Option                           | Description                                                                                                                |
+==================================+============================================================================================================================+
| Cores                            | Select virtual CPUs for the instance. For dedicated processing speed that others don't share, choose private. You can get  |
|                                  | up to 8 private cores and up to 16 public.                                                                                 |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Memory                           | Allocate RAM for the instance.                                                                                             |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Operating System                 | Select from a list of SoftLayer Linux or Windows images. Images are specific to the box service type, that is, Linux or    |
|                                  | Windows.                                                                                                                   |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| SSH Key                          | Select a public key to SSH into the Linux or Windows instance. The drop-down shows keys                                    |
|                                  | `added to your SoftLayer account <http://knowledgelayer.softlayer.com/procedure/add-ssh-key>`_.                            |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Instances                        | Specify the number of instances to provision.                                                                              |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+

**Block Devices**

By default, the machine is provisioned with 25GB local disk space. You can increase local system or portable SAN disk space. Get up to 400 local disk space or up to 2.1 TB of SAN storage.

**Network**

+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Option                           | Description                                                                                                                |
+==================================+============================================================================================================================+
| Datacenter                       | Select a location to place the instance.                                                                                   |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Uplink Port Speed                | Optionally, upgrade the speed of the instance network port. By default, it is 10 Mbps. But you can upgrade to 100 or 1000  |
|                                  | Mbps for private use, meaning no one else shares the network interface card port.                                          |
+----------------------------------+----------------------------------------------------------------------------------------------------------------------------+



