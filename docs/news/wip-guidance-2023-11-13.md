# Windows Information Protection guidance

In July 2022 Microsoft announced deprecation of certain capabilities within the solution known as Windows Information Protection (WIP), previously referred to as Enterprise Data Protection (EDP).

WIP as an offering is no longer under active feature development. The sunset process was announced [here](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/announcing-the-sunset-of-windows-information-protection-wip/ba-p/3579282).

Following this deprecation announcement, the Microsoft Endpoint Manager team announced ending support for the WIP *without enrollment* scenario by EOY 2022.

The announcement by the Microsoft Endpoint Manager team is [here](https://techcommunity.microsoft.com/t5/intune-customer-success/support-tip-end-of-support-guidance-for-windows-information/ba-p/3580091).

**NOTE: This only impacts unmanaged devices**. 

## Where does this leave me?

Your organisation falls into one of three categories:
1. You have already implemented the blueprint recommendations and you have at least some unmanaged devices, or
2. You have already implmented the blueprint recommendations and you only have managed devices.
3. You haven't yet implemented the blueprint recommended configurations

### Scenario 1:
If your organisation is using WIP without enrollment (unmanaged devices), Microsoft should have already been in touch with you about the impact to your devices and the timelines for that impact.

### Scenario 2:
If you are only using WIP with managed devices, Microsoft Endpoint Manager will continue to support WIP with enrollment (managed devices) for the duration of the Operating System (OS) lifecycle and will continue to offer options to enroll both corporate and personal devices for management (and subsequently to receive WIP policy).

**NOTE: There will be no feature updates and at some point Microsoft will drop support for this product. Probably good to add this to your roadmap.**

### Scenario 3:

For all new configurations we recommend using the Alternative Products / Features listed below. More information on the configuration of these is the subject of future work in early 2024.

1. Conditional Access + session controls using Microsoft Defender for Cloud Apps
2. Using Windows MAM (Only for unmanaged devices)
3. Leverage Tenant Restrictions to manage how SaaS and LOB applications are accessed
4. Leverage Endpoint DLP to define work vs non-work data boundaries

### These WIP features do not currently have an alternative

| Feature |  Description | Microsoft Status |
| --- | --- | --- |
| Unsanctioned Application Protections | Currently admins can define a set of sanctioned applications, with their own enforcement on activities. This Unsanctioned App Protection feature would extend this to unsanctioned applications as well. | In planning |
| Context based classification | This set of scenarios involves admins being able to scope protection to the context of where the file originates such as the originating source location or source application of the file. | In planning |
| Identity | Any protections that rely on the context of the user’s identity including identity separation in Outlook, Edge, and access within enlightened apps. These scenarios will not be supported in Purview. For user level restrictions, our guidance will be to use Tenant Level Restrictions within Azure AD. | Not Planned |

