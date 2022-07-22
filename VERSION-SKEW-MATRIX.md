# VERSION SKEW MATRIX
## Argus Releases
| name | version | appVersion | dependencies | Compatible Kubernetes Versions |
| :---- | :---- | :---- | :---- | :---- |
| argus | [2.1.0-rc01](https://github.com/logicmonitor/helm-charts-qa/releases/tag/argus-2.1.0-rc01) | [v8.1.0-rc1](https://hub.docker.com/r/logicmonitor/argus/tags?page=1&name=v8.1.0-rc1) | <ul> <li>kube-state-metrics@4.7.0 https://prometheus-community.github.io/helm-charts</li> </ul> | >= 1.16.0-0 | 
| argus | [2.0.0-rt01](https://github.com/logicmonitor/helm-charts-qa/releases/tag/argus-2.0.0-rt01) | [v8.0.0-rc9](https://hub.docker.com/r/logicmonitor/argus/tags?page=1&name=v8.0.0-rc9) | <ul> <li>kube-state-metrics@4.7.0 https://prometheus-community.github.io/helm-charts</li> </ul> | >= 1.16.0-0 | 
| argus | [2.0.0-rc994](https://github.com/logicmonitor/helm-charts-qa/releases/tag/argus-2.0.0-rc994) | [v8.0.0-rc9](https://hub.docker.com/r/logicmonitor/argus/tags?page=1&name=v8.0.0-rc9) | <ul> <li>kube-state-metrics@4.7.0 https://prometheus-community.github.io/helm-charts</li> </ul> | >= 1.16.0-0 | 

## Collectorset Controller Releases
| name | version | appVersion | dependencies | Compatible Kubernetes Versions |
| :---- | :---- | :---- | :---- | :---- |
| collectorset-controller | [1.0.0-rt01](https://github.com/logicmonitor/helm-charts-qa/releases/tag/collectorset-controller-1.0.0-rt01) | [v4.0.0-rc4](https://hub.docker.com/r/logicmonitor/collectorset-controller/tags?page=1&name=v4.0.0-rc4) | <ul>  </ul> | >= 1.16.0-0 | 
| collectorset-controller | [1.0.0-rc87](https://github.com/logicmonitor/helm-charts-qa/releases/tag/collectorset-controller-1.0.0-rc87) | [v4.0.0-rc3](https://hub.docker.com/r/logicmonitor/collectorset-controller/tags?page=1&name=v4.0.0-rc3) | <ul>  </ul> | >= 1.16.0-0 | 

## LM Container Releases
| name | version | appVersion | dependencies | Compatible Kubernetes Versions |
| :---- | :---- | :---- | :---- | :---- |
| lm-container | [1.1.0-rc01](https://github.com/logicmonitor/helm-charts-qa/releases/tag/lm-container-1.1.0-rc01) |  | <ul> <li>argus@2.1.0-rc01 https://logicmonitor.github.io/helm-charts-qa</li><li>collectorset-controller@1.0.0-rt01 https://logicmonitor.github.io/helm-charts-qa</li> </ul> | >= 1.16.0 | 
| lm-container | [1.0.0-rt01](https://github.com/logicmonitor/helm-charts-qa/releases/tag/lm-container-1.0.0-rt01) |  | <ul> <li>argus@2.0.0-rt01 https://logicmonitor.github.io/helm-charts-qa</li><li>collectorset-controller@1.0.0-rt01 https://logicmonitor.github.io/helm-charts-qa</li> </ul> | >= 1.16.0 | 
| lm-container | [1.0.0-rc998](https://github.com/logicmonitor/helm-charts-qa/releases/tag/lm-container-1.0.0-rc998) |  | <ul> <li>argus@2.0.0-rc994 https://logicmonitor.github.io/helm-charts-qa</li><li>collectorset-controller@1.0.0-rc87 https://logicmonitor.github.io/helm-charts-qa</li> </ul> | >= 1.16.0 | 