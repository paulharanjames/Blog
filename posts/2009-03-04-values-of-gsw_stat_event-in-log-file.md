
Last week, customer reported an issue &#8216;Campaign Callback rescheduled call details are missing&#8217; in the canned reports. After few hours of log analysis, it seems to be a defect in Genesys Dialer (OCS) and raised SR with support team.

  I found this tabular list very useful while debugging reports for dialer solution and hope you will find it useful too

 CampaignActivated = 1,

CampaignDeactivated = 2,

DialingStarted = 3,

DialModeChanged = 4,

DialingStopped = 5,

WaitingAgentStart = 6,

WaitingAgentOver = 7,

WaitingPortsStart = 8,

WaitingPortsOver = 9,

WaitingRecordsStart = 10,

WaitingRecordsOver = 11,

SystemErrorStart = 12,

SystemErrorOver = 13,

CallCompleted = 14,

LeadProcessed = 15,

CallbackScheduled = 16,

CallbackCompleted = 17,

CallbackMissed = 18,

AgentError = 19,

RecordScheduled = 20,