# Fabric8 Kubernetes Client 7.0.0

https://github.com/fabric8io/kubernetes-client/issues/5778

Preparation work for the upcoming release of Fabric8 Kubernetes Client 7.0.0.

## 6.x Required changes

Additional work for a last minor 6.x release before we start working on version 7.

- Deprecations

## 7.0.0 Goals

- Documentation and ADRs
  - Maybe a good moment to add a minimal website (antora, etc.) too
- Java 11
  - https://github.com/sundrio/sundrio/issues/464#issuecomment-2025563980
  - https://github.com/sundrio/sundrio/issues/466
  - https://github.com/sundrio/sundrio/pull/467
- Migration guide
  - ✅ https://github.com/fabric8io/kubernetes-client/pull/5779
- `withReadyWaitTimeout` operations (log, exec, upload) can default to 0 instead of 5 and make it opt-in:
  - https://github.com/fabric8io/kubernetes-client/issues/5782#issuecomment-1985617986
- Further handling of the CustomResource class
  - https://github.com/fabric8io/kubernetes-client/issues/2829#issuecomment-1197676790
  - HasStatus https://github.com/fabric8io/kubernetes-client/issues/3586<br/>
    HasSpec https://github.com/fabric8io/kubernetes-client/issues/3816
  - Mark CRD spec as required (HasStatus, HasSpec -marked as required-)<br />
    https://github.com/fabric8io/kubernetes-client/issues/3096
- OpenShiftMockServer is removed
  - https://github.com/fabric8io/kubernetes-client/issues/5351
- SupportTestingClient interface is removed
  - https://github.com/fabric8io/kubernetes-client/issues/4659
- Bump OkHttp to latest major (4.x)
  - https://github.com/fabric8io/kubernetes-client/issues/2632
- Consider Migrating deprecated Felix Annotations to OSGi component Annotations
  - https://github.com/fabric8io/kubernetes-client/issues/4445
- Vert.x HttpClient is now the default HTTP client implementation (as opposed to OkHttp)
- MockWebServer is based on Vert.x
  - https://github.com/fabric8io/kubernetes-client/issues/5719
  - https://github.com/fabric8io/kubernetes-client/pull/5632
- After MockWebServer refactor, fix problem with @Nested
  - https://github.com/fabric8io/kubernetes-client/issues/3032
  - https://github.com/fabric8io/kubernetes-client/issues/4649
- After MockWebServer refactor, MockWebServer HTTP/2 support
  - https://github.com/fabric8io/kubernetes-client/issues/4193
- Use a single `@Resource` annotation (instead of Plural, Group, Kind, etc.)
  - https://github.com/fabric8io/kubernetes-client/issues/4164
- Improve logging configuration experience
  - https://github.com/fabric8io/kubernetes-client/issues/4625
- Remove (some) deprecated APIs
  - https://github.com/fabric8io/kubernetes-client/issues/4956
- Move interceptors to their own package
  - https://github.com/fabric8io/kubernetes-client/issues/5111
- Remove deprecated Config.errorMessages field
  - https://github.com/fabric8io/kubernetes-client/issues/5264
- Remove OpenShift MockServer
  - https://github.com/fabric8io/kubernetes-client/issues/5351
- ZJSONPatch
  - https://github.com/fabric8io/kubernetes-client/issues/5480
- Default owner reference blockOwnerDeletion to true
  - https://github.com/fabric8io/kubernetes-client/issues/5838
