# Spot Instances
Last Updated: {{ git_revision_date_localized }}

![](../images/aws-ec2-spot-view.drawio..svg)

## Some Key Points relative to the picture above
1. A Spot Fleet enables you to have a "hybrid" combination that includes Spot instance types AND On-Demand Instances if you don't necessarily want to loose it all, but you want to take advantage of Spot pricing for some capacity.  
1. i.e. you need to write the app so it can handle the loss of nodes.

__NOTE: You can right click on the image and download it. Each diagram is an SVG file created using DrawIO. That means you can edit the downloaded file with DrawIO__
