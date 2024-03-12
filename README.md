# Fabric8 Kubernetes Client 7.0.0

https://github.com/fabric8io/kubernetes-client/issues/5778

Preparation work for the upcoming release of Fabric8 Kubernetes Client 7.0.0.

## WIP

Currently checking the open issues at Fabric8 Kubernetes Client repository
Last issue checked in the list (https://github.com/fabric8io/kubernetes-client/issues?page=3&q=is%3Aissue+is%3Aopen): https://github.com/fabric8io/kubernetes-client/issues/4659

## 6.x Required changes

Additional work for a last minor 6.x release before we start working on version 7.


## 7.0.0 Goals

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
