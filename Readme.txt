Let’s recap,
we have a Prometheus instance on an AWS EC2 instance configured to discover services on port 9100 
in the same network and one Node Exporter instance collecting OS metrics that can be easily upgraded 
to many Node Exporter instances as desired.
But we are not done yet,we don’t want to be monitoring by ourselves.
Prometheus can send us an alert to an email when it finds something.
Let’s configure some rules and Prometheus Alertmanager with a Gmail account to accomplish this.
“The Alertmanager handles alerts sent by client applications such as the Prometheus server. 
It takes care of deduplicating, grouping, and routing them to the correct receiver integrations such as email,
PagerDuty, or OpsGenie. It also takes care of silencing and inhibition of alerts