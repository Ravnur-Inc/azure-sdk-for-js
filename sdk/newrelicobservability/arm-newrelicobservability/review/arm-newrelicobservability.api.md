## API Report File for "@azure/arm-newrelicobservability"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import * as coreAuth from '@azure/core-auth';
import * as coreClient from '@azure/core-client';
import { OperationState } from '@azure/core-lro';
import { PagedAsyncIterableIterator } from '@azure/core-paging';
import { SimplePollerLike } from '@azure/core-lro';

// @public
export type AccountCreationSource = string;

// @public
export interface AccountInfo {
    accountId?: string;
    ingestionKey?: string;
    region?: string;
}

// @public
export interface AccountResource extends ProxyResource {
    accountId?: string;
    accountName?: string;
    organizationId?: string;
    region?: string;
}

// @public
export interface Accounts {
    list(userEmail: string, location: string, options?: AccountsListOptionalParams): PagedAsyncIterableIterator<AccountResource>;
}

// @public
export interface AccountsListNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type AccountsListNextResponse = AccountsListResponse;

// @public
export type AccountsListOperationResponse = AccountsListResponse;

// @public
export interface AccountsListOptionalParams extends coreClient.OperationOptions {
}

// @public
export interface AccountsListResponse {
    nextLink?: string;
    value: AccountResource[];
}

// @public
export type ActionType = string;

// @public
export interface AppServiceInfo {
    agentStatus?: string;
    agentVersion?: string;
    azureResourceId?: string;
}

// @public
export interface AppServicesGetParameter {
    request: AppServicesGetRequest;
}

// @public
export interface AppServicesGetRequest {
    azureResourceIds?: string[];
    userEmail: string;
}

// @public
export interface AppServicesListResponse {
    nextLink?: string;
    value: AppServiceInfo[];
}

// @public
export type BillingCycle = string;

// @public
export type BillingSource = string;

// @public
export type CreatedByType = string;

// @public
export interface ErrorAdditionalInfo {
    readonly info?: Record<string, unknown>;
    readonly type?: string;
}

// @public
export interface ErrorDetail {
    readonly additionalInfo?: ErrorAdditionalInfo[];
    readonly code?: string;
    readonly details?: ErrorDetail[];
    readonly message?: string;
    readonly target?: string;
}

// @public
export interface ErrorResponse {
    error?: ErrorDetail;
}

// @public
export interface FilteringTag {
    action?: TagAction;
    name?: string;
    value?: string;
}

// @public
export function getContinuationToken(page: unknown): string | undefined;

// @public
export interface HostsGetParameter {
    request: HostsGetRequest;
}

// @public
export interface HostsGetRequest {
    userEmail: string;
    vmIds?: string[];
}

// @public
export enum KnownAccountCreationSource {
    Liftr = "LIFTR",
    Newrelic = "NEWRELIC"
}

// @public
export enum KnownActionType {
    Internal = "Internal"
}

// @public
export enum KnownBillingCycle {
    Monthly = "MONTHLY",
    Weekly = "WEEKLY",
    Yearly = "YEARLY"
}

// @public
export enum KnownBillingSource {
    Azure = "AZURE",
    Newrelic = "NEWRELIC"
}

// @public
export enum KnownCreatedByType {
    Application = "Application",
    Key = "Key",
    ManagedIdentity = "ManagedIdentity",
    User = "User"
}

// @public
export enum KnownLiftrResourceCategories {
    MonitorLogs = "MonitorLogs",
    Unknown = "Unknown"
}

// @public
export enum KnownManagedServiceIdentityType {
    None = "None",
    SystemAssigned = "SystemAssigned",
    SystemAssignedUserAssigned = "SystemAssigned, UserAssigned",
    UserAssigned = "UserAssigned"
}

// @public
export enum KnownMarketplaceSubscriptionStatus {
    Active = "Active",
    Suspended = "Suspended"
}

// @public
export enum KnownMonitoringStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownOrgCreationSource {
    Liftr = "LIFTR",
    Newrelic = "NEWRELIC"
}

// @public
export enum KnownOrigin {
    System = "system",
    User = "user",
    UserSystem = "user,system"
}

// @public
export enum KnownProvisioningState {
    Accepted = "Accepted",
    Canceled = "Canceled",
    Creating = "Creating",
    Deleted = "Deleted",
    Deleting = "Deleting",
    Failed = "Failed",
    NotSpecified = "NotSpecified",
    Succeeded = "Succeeded",
    Updating = "Updating"
}

// @public
export enum KnownSendAadLogsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSendActivityLogsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSendingLogsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSendingMetricsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSendMetricsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSendSubscriptionLogsStatus {
    Disabled = "Disabled",
    Enabled = "Enabled"
}

// @public
export enum KnownSingleSignOnStates {
    Disable = "Disable",
    Enable = "Enable",
    Existing = "Existing",
    Initial = "Initial"
}

// @public
export enum KnownTagAction {
    Exclude = "Exclude",
    Include = "Include"
}

// @public
export enum KnownUsageType {
    Committed = "COMMITTED",
    Payg = "PAYG"
}

// @public
export type LiftrResourceCategories = string;

// @public
export interface LogRules {
    filteringTags?: FilteringTag[];
    sendAadLogs?: SendAadLogsStatus;
    sendActivityLogs?: SendActivityLogsStatus;
    sendSubscriptionLogs?: SendSubscriptionLogsStatus;
}

// @public
export interface ManagedServiceIdentity {
    readonly principalId?: string;
    readonly tenantId?: string;
    type: ManagedServiceIdentityType;
    userAssignedIdentities?: {
        [propertyName: string]: UserAssignedIdentity;
    };
}

// @public
export type ManagedServiceIdentityType = string;

// @public
export type MarketplaceSubscriptionStatus = string;

// @public
export interface MetricRules {
    filteringTags?: FilteringTag[];
    sendMetrics?: SendMetricsStatus;
    userEmail?: string;
}

// @public
export interface MetricsRequest {
    userEmail: string;
}

// @public
export interface MetricsRequestParameter {
    request: MetricsRequest;
}

// @public
export interface MetricsStatusRequest {
    azureResourceIds?: string[];
    userEmail: string;
}

// @public
export interface MetricsStatusRequestParameter {
    request: MetricsStatusRequest;
}

// @public
export interface MetricsStatusResponse {
    azureResourceIds?: string[];
}

// @public
export interface MonitoredResource {
    id?: string;
    reasonForLogsStatus?: string;
    reasonForMetricsStatus?: string;
    sendingLogs?: SendingLogsStatus;
    sendingMetrics?: SendingMetricsStatus;
}

// @public
export interface MonitoredResourceListResponse {
    nextLink?: string;
    value: MonitoredResource[];
}

// @public
export type MonitoringStatus = string;

// @public
export interface Monitors {
    beginCreateOrUpdate(resourceGroupName: string, monitorName: string, resource: NewRelicMonitorResource, options?: MonitorsCreateOrUpdateOptionalParams): Promise<SimplePollerLike<OperationState<MonitorsCreateOrUpdateResponse>, MonitorsCreateOrUpdateResponse>>;
    beginCreateOrUpdateAndWait(resourceGroupName: string, monitorName: string, resource: NewRelicMonitorResource, options?: MonitorsCreateOrUpdateOptionalParams): Promise<MonitorsCreateOrUpdateResponse>;
    beginDelete(resourceGroupName: string, userEmail: string, monitorName: string, options?: MonitorsDeleteOptionalParams): Promise<SimplePollerLike<OperationState<void>, void>>;
    beginDeleteAndWait(resourceGroupName: string, userEmail: string, monitorName: string, options?: MonitorsDeleteOptionalParams): Promise<void>;
    get(resourceGroupName: string, monitorName: string, options?: MonitorsGetOptionalParams): Promise<MonitorsGetResponse>;
    getMetricRules(resourceGroupName: string, monitorName: string, request: MetricsRequest, options?: MonitorsGetMetricRulesOptionalParams): Promise<MonitorsGetMetricRulesResponse>;
    getMetricStatus(resourceGroupName: string, monitorName: string, request: MetricsStatusRequest, options?: MonitorsGetMetricStatusOptionalParams): Promise<MonitorsGetMetricStatusResponse>;
    listAppServices(resourceGroupName: string, monitorName: string, request: AppServicesGetRequest, options?: MonitorsListAppServicesOptionalParams): PagedAsyncIterableIterator<AppServiceInfo>;
    listByResourceGroup(resourceGroupName: string, options?: MonitorsListByResourceGroupOptionalParams): PagedAsyncIterableIterator<NewRelicMonitorResource>;
    listBySubscription(options?: MonitorsListBySubscriptionOptionalParams): PagedAsyncIterableIterator<NewRelicMonitorResource>;
    listHosts(resourceGroupName: string, monitorName: string, request: HostsGetRequest, options?: MonitorsListHostsOptionalParams): PagedAsyncIterableIterator<VMInfo>;
    listMonitoredResources(resourceGroupName: string, monitorName: string, options?: MonitorsListMonitoredResourcesOptionalParams): PagedAsyncIterableIterator<MonitoredResource>;
    switchBilling(resourceGroupName: string, monitorName: string, request: SwitchBillingRequest, options?: MonitorsSwitchBillingOptionalParams): Promise<void>;
    update(resourceGroupName: string, monitorName: string, properties: NewRelicMonitorResourceUpdate, options?: MonitorsUpdateOptionalParams): Promise<MonitorsUpdateResponse>;
    vmHostPayload(resourceGroupName: string, monitorName: string, options?: MonitorsVmHostPayloadOptionalParams): Promise<MonitorsVmHostPayloadResponse>;
}

// @public
export interface MonitorsCreateOrUpdateHeaders {
    retryAfter?: number;
}

// @public
export interface MonitorsCreateOrUpdateOptionalParams extends coreClient.OperationOptions {
    resumeFrom?: string;
    updateIntervalInMs?: number;
}

// @public
export type MonitorsCreateOrUpdateResponse = NewRelicMonitorResource;

// @public
export interface MonitorsDeleteHeaders {
    retryAfter?: number;
}

// @public
export interface MonitorsDeleteOptionalParams extends coreClient.OperationOptions {
    resumeFrom?: string;
    updateIntervalInMs?: number;
}

// @public
export interface MonitorsGetMetricRulesOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsGetMetricRulesResponse = MetricRules;

// @public
export interface MonitorsGetMetricStatusOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsGetMetricStatusResponse = MetricsStatusResponse;

// @public
export interface MonitorsGetOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsGetResponse = NewRelicMonitorResource;

// @public
export interface MonitorsListAppServicesNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListAppServicesNextResponse = AppServicesListResponse;

// @public
export interface MonitorsListAppServicesOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListAppServicesResponse = AppServicesListResponse;

// @public
export interface MonitorsListByResourceGroupNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListByResourceGroupNextResponse = NewRelicMonitorResourceListResult;

// @public
export interface MonitorsListByResourceGroupOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListByResourceGroupResponse = NewRelicMonitorResourceListResult;

// @public
export interface MonitorsListBySubscriptionNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListBySubscriptionNextResponse = NewRelicMonitorResourceListResult;

// @public
export interface MonitorsListBySubscriptionOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListBySubscriptionResponse = NewRelicMonitorResourceListResult;

// @public
export interface MonitorsListHostsNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListHostsNextResponse = VMHostsListResponse;

// @public
export interface MonitorsListHostsOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListHostsResponse = VMHostsListResponse;

// @public
export interface MonitorsListMonitoredResourcesNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListMonitoredResourcesNextResponse = MonitoredResourceListResponse;

// @public
export interface MonitorsListMonitoredResourcesOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsListMonitoredResourcesResponse = MonitoredResourceListResponse;

// @public
export interface MonitorsSwitchBillingOptionalParams extends coreClient.OperationOptions {
}

// @public
export interface MonitorsUpdateOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsUpdateResponse = NewRelicMonitorResource;

// @public
export interface MonitorsVmHostPayloadOptionalParams extends coreClient.OperationOptions {
}

// @public
export type MonitorsVmHostPayloadResponse = VMExtensionPayload;

// @public
export interface NewRelicAccountProperties {
    accountInfo?: AccountInfo;
    organizationInfo?: OrganizationInfo;
    singleSignOnProperties?: NewRelicSingleSignOnProperties;
    userId?: string;
}

// @public
export interface NewRelicMonitorResource extends TrackedResource {
    accountCreationSource?: AccountCreationSource;
    identity?: ManagedServiceIdentity;
    readonly liftrResourceCategory?: LiftrResourceCategories;
    readonly liftrResourcePreference?: number;
    readonly marketplaceSubscriptionId?: string;
    readonly marketplaceSubscriptionStatus?: MarketplaceSubscriptionStatus;
    readonly monitoringStatus?: MonitoringStatus;
    newRelicAccountProperties?: NewRelicAccountProperties;
    orgCreationSource?: OrgCreationSource;
    planData?: PlanData;
    readonly provisioningState?: ProvisioningState;
    userInfo?: UserInfo;
}

// @public
export interface NewRelicMonitorResourceListResult {
    nextLink?: string;
    value: NewRelicMonitorResource[];
}

// @public
export interface NewRelicMonitorResourceUpdate {
    accountCreationSource?: AccountCreationSource;
    identity?: ManagedServiceIdentity;
    newRelicAccountProperties?: NewRelicAccountProperties;
    orgCreationSource?: OrgCreationSource;
    planData?: PlanData;
    tags?: {
        [propertyName: string]: string;
    };
    userInfo?: UserInfo;
}

// @public (undocumented)
export class NewRelicObservability extends coreClient.ServiceClient {
    // (undocumented)
    $host: string;
    constructor(credentials: coreAuth.TokenCredential, subscriptionId: string, options?: NewRelicObservabilityOptionalParams);
    // (undocumented)
    accounts: Accounts;
    // (undocumented)
    apiVersion: string;
    // (undocumented)
    monitors: Monitors;
    // (undocumented)
    operations: Operations;
    // (undocumented)
    organizations: Organizations;
    // (undocumented)
    plans: Plans;
    // (undocumented)
    subscriptionId: string;
    // (undocumented)
    tagRules: TagRules;
}

// @public
export interface NewRelicObservabilityOptionalParams extends coreClient.ServiceClientOptions {
    $host?: string;
    apiVersion?: string;
    endpoint?: string;
}

// @public
export interface NewRelicSingleSignOnProperties {
    enterpriseAppId?: string;
    provisioningState?: ProvisioningState;
    singleSignOnState?: SingleSignOnStates;
    singleSignOnUrl?: string;
}

// @public
export interface Operation {
    readonly actionType?: ActionType;
    display?: OperationDisplay;
    readonly isDataAction?: boolean;
    readonly name?: string;
    readonly origin?: Origin;
}

// @public
export interface OperationDisplay {
    readonly description?: string;
    readonly operation?: string;
    readonly provider?: string;
    readonly resource?: string;
}

// @public
export interface OperationListResult {
    readonly nextLink?: string;
    readonly value?: Operation[];
}

// @public
export interface Operations {
    list(options?: OperationsListOptionalParams): PagedAsyncIterableIterator<Operation>;
}

// @public
export interface OperationsListNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type OperationsListNextResponse = OperationListResult;

// @public
export interface OperationsListOptionalParams extends coreClient.OperationOptions {
}

// @public
export type OperationsListResponse = OperationListResult;

// @public
export interface OrganizationInfo {
    organizationId?: string;
}

// @public
export interface OrganizationResource extends ProxyResource {
    billingSource?: BillingSource;
    organizationId?: string;
    organizationName?: string;
}

// @public
export interface Organizations {
    list(userEmail: string, location: string, options?: OrganizationsListOptionalParams): PagedAsyncIterableIterator<OrganizationResource>;
}

// @public
export interface OrganizationsListNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type OrganizationsListNextResponse = OrganizationsListResponse;

// @public
export type OrganizationsListOperationResponse = OrganizationsListResponse;

// @public
export interface OrganizationsListOptionalParams extends coreClient.OperationOptions {
}

// @public
export interface OrganizationsListResponse {
    nextLink?: string;
    value: OrganizationResource[];
}

// @public
export type OrgCreationSource = string;

// @public
export type Origin = string;

// @public
export interface PlanData {
    billingCycle?: BillingCycle;
    effectiveDate?: Date;
    planDetails?: string;
    usageType?: UsageType;
}

// @public
export interface PlanDataListResponse {
    nextLink?: string;
    value: PlanDataResource[];
}

// @public
export interface PlanDataResource extends ProxyResource {
    accountCreationSource?: AccountCreationSource;
    orgCreationSource?: OrgCreationSource;
    planData?: PlanData;
}

// @public
export interface Plans {
    list(options?: PlansListOptionalParams): PagedAsyncIterableIterator<PlanDataResource>;
}

// @public
export interface PlansListNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type PlansListNextResponse = PlanDataListResponse;

// @public
export interface PlansListOptionalParams extends coreClient.OperationOptions {
    accountId?: string;
    organizationId?: string;
}

// @public
export type PlansListResponse = PlanDataListResponse;

// @public
export type ProvisioningState = string;

// @public
export interface ProxyResource extends Resource {
}

// @public
export interface Resource {
    readonly id?: string;
    readonly name?: string;
    readonly systemData?: SystemData;
    readonly type?: string;
}

// @public
export type SendAadLogsStatus = string;

// @public
export type SendActivityLogsStatus = string;

// @public
export type SendingLogsStatus = string;

// @public
export type SendingMetricsStatus = string;

// @public
export type SendMetricsStatus = string;

// @public
export type SendSubscriptionLogsStatus = string;

// @public
export type SingleSignOnStates = string;

// @public
export interface SwitchBillingParameter {
    request: SwitchBillingRequest;
}

// @public
export interface SwitchBillingRequest {
    azureResourceId?: string;
    organizationId?: string;
    planData?: PlanData;
    userEmail: string;
}

// @public
export interface SystemData {
    createdAt?: Date;
    createdBy?: string;
    createdByType?: CreatedByType;
    lastModifiedAt?: Date;
    lastModifiedBy?: string;
    lastModifiedByType?: CreatedByType;
}

// @public
export type TagAction = string;

// @public
export interface TagRule extends ProxyResource {
    logRules?: LogRules;
    metricRules?: MetricRules;
    readonly provisioningState?: ProvisioningState;
}

// @public
export interface TagRuleListResult {
    nextLink?: string;
    value: TagRule[];
}

// @public
export interface TagRules {
    beginCreateOrUpdate(resourceGroupName: string, monitorName: string, ruleSetName: string, resource: TagRule, options?: TagRulesCreateOrUpdateOptionalParams): Promise<SimplePollerLike<OperationState<TagRulesCreateOrUpdateResponse>, TagRulesCreateOrUpdateResponse>>;
    beginCreateOrUpdateAndWait(resourceGroupName: string, monitorName: string, ruleSetName: string, resource: TagRule, options?: TagRulesCreateOrUpdateOptionalParams): Promise<TagRulesCreateOrUpdateResponse>;
    beginDelete(resourceGroupName: string, monitorName: string, ruleSetName: string, options?: TagRulesDeleteOptionalParams): Promise<SimplePollerLike<OperationState<void>, void>>;
    beginDeleteAndWait(resourceGroupName: string, monitorName: string, ruleSetName: string, options?: TagRulesDeleteOptionalParams): Promise<void>;
    get(resourceGroupName: string, monitorName: string, ruleSetName: string, options?: TagRulesGetOptionalParams): Promise<TagRulesGetResponse>;
    listByNewRelicMonitorResource(resourceGroupName: string, monitorName: string, options?: TagRulesListByNewRelicMonitorResourceOptionalParams): PagedAsyncIterableIterator<TagRule>;
    update(resourceGroupName: string, monitorName: string, ruleSetName: string, properties: TagRuleUpdate, options?: TagRulesUpdateOptionalParams): Promise<TagRulesUpdateResponse>;
}

// @public
export interface TagRulesCreateOrUpdateHeaders {
    retryAfter?: number;
}

// @public
export interface TagRulesCreateOrUpdateOptionalParams extends coreClient.OperationOptions {
    resumeFrom?: string;
    updateIntervalInMs?: number;
}

// @public
export type TagRulesCreateOrUpdateResponse = TagRule;

// @public
export interface TagRulesDeleteHeaders {
    retryAfter?: number;
}

// @public
export interface TagRulesDeleteOptionalParams extends coreClient.OperationOptions {
    resumeFrom?: string;
    updateIntervalInMs?: number;
}

// @public
export interface TagRulesGetOptionalParams extends coreClient.OperationOptions {
}

// @public
export type TagRulesGetResponse = TagRule;

// @public
export interface TagRulesListByNewRelicMonitorResourceNextOptionalParams extends coreClient.OperationOptions {
}

// @public
export type TagRulesListByNewRelicMonitorResourceNextResponse = TagRuleListResult;

// @public
export interface TagRulesListByNewRelicMonitorResourceOptionalParams extends coreClient.OperationOptions {
}

// @public
export type TagRulesListByNewRelicMonitorResourceResponse = TagRuleListResult;

// @public
export interface TagRulesUpdateOptionalParams extends coreClient.OperationOptions {
}

// @public
export type TagRulesUpdateResponse = TagRule;

// @public
export interface TagRuleUpdate {
    logRules?: LogRules;
    metricRules?: MetricRules;
}

// @public
export interface TrackedResource extends Resource {
    location: string;
    tags?: {
        [propertyName: string]: string;
    };
}

// @public
export type UsageType = string;

// @public
export interface UserAssignedIdentity {
    readonly clientId?: string;
    readonly principalId?: string;
}

// @public
export interface UserInfo {
    country?: string;
    emailAddress?: string;
    firstName?: string;
    lastName?: string;
    phoneNumber?: string;
}

// @public
export interface VMExtensionPayload {
    ingestionKey?: string;
}

// @public
export interface VMHostsListResponse {
    nextLink?: string;
    value: VMInfo[];
}

// @public
export interface VMInfo {
    agentStatus?: string;
    agentVersion?: string;
    vmId?: string;
}

// (No @packageDocumentation comment for this package)

```