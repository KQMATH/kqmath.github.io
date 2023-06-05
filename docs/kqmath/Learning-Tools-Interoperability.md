# Learning Tools Interoperability (LTI)

[Learning Tools Interoperability](https://www.imsglobal.org/activity/learning-tools-interoperability) (LTI) is a standard created by the [IMS Global Learning Consortium](https://www.imsglobal.org) that links content and resources to learning platforms.

Its primary purpose is to connect learning systems such as a [learning management system](https://en.wikipedia.org/wiki/Learning_management_system) (LMS) with external service tools in a standard way across learning systems. The standard describes the connecting system as an LTI Tool Consumer and the connected tool as an LTI Tool Provider.

For a basic overview of how LTI works, see https://www.imsglobal.org/basic-overview-how-lti-works.

## Moodle as an LTI Tool provider
Moodle uses the built in '**Publish as LTI tool**' enrolment plugin, together with the '**LTI authentication plugin**', to allow remote users on a different site (known as an LTI consumer) to access selected courses and activities. In other words, moodle functions as an LTI tool provider. Grades are sent back to the remote system.

If your moodle instance is using HTTP (and not HTTPS) you will only be able to use the tool on sites that are also using HTTP (and not HTTPS). It's recommended that you use HTTPS on your moodle instance. See Transitioning to HTTPS

### LTI version support
<table>
    <tbody>
    <tr>
        <th>LTI version</th>
        <th>Moodle version</th>
    </tr>
    <tr>
        <td>LTI v1.0</td>
        <td>Moodle v2.6</td>
    </tr>
    <tr>
        <td>LTI v1.1</td>
        <td>Moodle v2.6</td>
    </tr>
    <tr>
        <td>LTI v2.0</td>
        <td>Moodle v2.8</td>
    </tr>
    <tr>
        <td>LTI v1.3</td>
        <td>Moodle v3.7</td>
    </tr>
    </tbody>
</table>


### Setup
#### Enabling 'Publish as LTI tool' at site level
An administrator can enable the 'Publish as LTI tool' for use across the site:

1. Go to `Site administration > Plugins > Authentication > Manage authentication` and enable 'LTI'.
2. Go to `Site administration > Plugins > Enrolments > Manage enrol plugins` and enable 'Publish as LTI tool'.

It is recommended that the site administration setting 'Allow frame embedding' is enabled (in `Site Administration > Security > HTTP security`) so that tools are displayed within a frame rather than in a new window.

#### Sharing access to a course or activity
1. Go to the 'Enrolment methods' page and add 'Publish as LTI tool' as an enrolment method
2. In 'Tool to be published' select the course or activity to be shared
3. Click the 'Add method' button
4. Go to `Course Administration > Published as LTI tools` page (`/enrol/lti/index.php?courseid=n`) and make a note of the launch details or the registration URL for the LTI consumer site (see below for info on which to choose). The URL will be of the form: `.../enrol/lti/...`
5. You will also need to give the LTI consumer site a consumer key - this can be anything you want.

The LTI consumer can be another Moodle site or any other LTI-consumer-compliant LMS, such as Blackboard. Depending on the requirements of the LTI consumer, you can provide either a cartridge URL (also called configuration URL) plus secret OR a launch URL (new in Moodle 3.5.2) OR a registration URL.

### Grading and user synchronization
Grade and user synchronization (if required) are done via the 'Publish as LTI tool grade sync' and 'Publish as LTI tool users sync' scheduled tasks. This is a [Cron](https://docs.moodle.org/en/Cron) task and is by default run every 30 minutes.

If user synchronisation is set to yes, enrolled users in the remote system are synchronised with enrolments in the course, with an account created for each remote user as necessary, and the user enrolled or unenrolled as required. If set to no, at the moment when a remote user accesses the tool, an account will be created for them and they will be automatically enrolled.

## Moodle as an LTI Tool consumer
### Setup
1. Visit a course.
2. Add a LTI activity.
   1. Use the URL and secret from the LTI provider site
   2. Enter any consumer key you want. This can be thought of as a username used to authenticate access to the tool. It can be used by the tool provider to uniquely identify the Moodle site from which the users launch into the tool. If you provide the same consumer key in another LTI activity, you will maintain your progress/session in the external resource (reuses the same user).
3. If you would like to not show blocks for teachers, you can pass the custom parameter "`force_embed = 1`". This may limit the functionality available to teachers and admins. To get blocks back, simply remove the parameter.
4. Log in as a student.
5. Visit the course and click on the LTI activity.
6. Check the activity displays as expected.

## Blackboard as an LTI Tool provider

## Blackboard as an LTI Tool consumer

## IMS specs support
<table>
    <tbody>
    <tr>
        <th>IMS Spec</th>
        <th>Moodle</th>
        <th>Canvas</th>
        <th>Edu app center (Canvas)</th>
        <th>Desire2Learn</th>
        <th>Blackboard</th>
        <th>Sakai</th>
    </tr>
    <tr>
        <td>Tool consumer</td>
        <td>External Tool</td>
        <td>External App</td>
        <td>App</td>
        <td>Link</td>
        <td>LTI Tool provider*</td>
        <td>Sakai Basic LTI portlet</td>
    </tr>
    <tr>
        <td>Launch URL</td>
        <td>Tool URL</td>
        <td>Launch URL</td>
        <td>n/a</td>
        <td>URL</td>
        <td>Provider Domain</td>
        <td>Remote Tool URL</td>
    </tr>
    <tr>
        <td>Secret</td>
        <td>Secret</td>
        <td>Secret</td>
        <td>Secret</td>
        <td>Secret</td>
        <td>Tool Provider Secret</td>
        <td>Remote tool secret</td>
    </tr>
    <tr>
        <td>Cartridge URL</td>
        <td>Tool URL</td>
        <td>Paste XML</td>
        <td>Configuration URL</td>
        <td>n/a</td>
        <td>n/a</td>
        <td>Tool registration file?</td>
    </tr>
    <tr>
        <td>Proxy URL</td>
        <td>Registration URL/Tool URL</td>
        <td>LTI 2 Registration URL</td>
        <td>n/a</td>
        <td>n/a</td>
        <td>n/a</td>
        <td>-</td>
    </tr>
    </tbody>
</table>

## LTI versions
LTI 1 actually means a launch URL (which is compatible with LTI 1 or LTI 2 compliant consumers).  
LTI 2 actually means a proxy (which is compatible with LTI 2 compliant consumers).
<table>
    <tbody>
    <tr>
        <th>Feature</td>
        <th>LTI 1.0</td>
        <th>LTI 1.1</td>
        <th>LTI 1.2</td>
        <th>LTI 2.0</td>
        <th>Comment</td>
    </tr>
    <tr>
        <td>Basic Launch</td>
        <td>X</td>
        <td>X</td>
        <td>X</td>
        <td>X</td>
        <td>LTI 2+ greatly reduces requirements for optional data to be carried in every launch.
        </td>
    </tr>
    <tr>
        <td>Simple Outcomes</td>
        <td></td>
        <td>X</td>
        <td>X</td>
        <td>X</td>
        <td>Return single numeric value that scores the value of launch activity.
        </td>
    </tr>
    <tr>
        <td>Tool Consumer Profile</td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>X</td>
        <td>TCP is metadata that describes attributes and available services of the Tool Consumer. &nbsp;It's made available by a
            REST service.
        </td>
    </tr>
    <tr>
        <td>Tool Proxy</td>
        <td></td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>TP is metadata that describes the negotiated interface contract between a particular ToolConsumer and ToolProvider.
        </td>
    </tr>
    <tr>
        <td>Credential Management</td>
        <td></td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>Automatic secure exchange of key/secret</td>
    </tr>
    <tr>
        <td>Registration Flow</td>
        <td></td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>LMS Admin initiates new tool provisioning including tool proxy creation and credential management.
        </td>
    </tr>
    <tr>
        <td>Reregistration Flow</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>LMS Admin initiates an existing tool reprovisioning.</td>
    </tr>
    <tr>
        <td>Model-driven documentation</td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>X</td>
        <td>Tool-generated, exhaustive, reference documentation generated from UML
        </td>
    </tr>
    <tr>
        <td>REST services</td>
        <td></td>
        <td></td>
        <td>X</td>
        <td>X</td>
        <td>REST level 3 services for a variety of server-to-server tasks. Note that LTI 1.2 limits REST service implementation to
            be on ToolConsumer only.
        </td>
    </tr>
    </tbody>
</table>
