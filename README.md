# ApplitoolsTestResultsHandler - Javascript
### v2.0.0

The Applitools Test Results Handler extends the capabilities of TestResults with additional API calls.
With these additional API calls you will be able to retrive additional details at the end of the test.

Note: The Test Results Handler requires your account View Key - which can be found in the admin panel. Contact Applitools support at support@applitools.com if you need further assistance retrieving it.

## The images that can be downloaded are:

- The test baseline image - Unless specified, the images will be downloaded to the working directory.

- The actual images - Unless specified, the images will be downloaded to the working directory.

- The images with the differences highlighted - Unless specified, the images will be downloaded to the working directory.

- Get the status of each step [Missing, Unresolved, Passed, New]

### How to use the tool:

##### To initialize the Handler:
```javascript
let results = await eyes.close(false);
const handler= new ApplitoolsTestResultHandler(results, applitoolsViewKey);
```

##### **downloadDiffs** -  Downloading the test images with the highlighted detected differences to a given directory. In case of New, Missing or passed step no image will be downloaded.
```javascript
handler.downloadImages(downloadDir, 'diff')
```

##### **downloadBaselineImages** -  Downloading the test baseline images to a given directory
```javascript
handler.downloadImages(downloadDir, 'baseline');
```

##### **downloadCurrentImages** -  Downloading the test current image to a given directory.
```javascript
handler.downloadImages(downloadDir, 'current');
```

# Further regarding:

Getting Diff Images Manually - http://support.applitools.com/customer/portal/articles/2457891 
Getting Current/Baseline Images Manually - http://support.applitools.com/customer/portal/articles/2917372
Extend API features with EyesUtilities - http://support.applitools.com/customer/portal/articles/2913152