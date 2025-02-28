# Unmanage an account<a name="unmanage-account"></a>

If you created an account in Account Factory or enrolled an AWS account, and you no longer want the account to be managed by AWS Control Tower in a landing zone, you can unmanage the account from the AWS Control Tower console\. 

When you unmanage an AWS Control Tower account, all resources provisioned by AWS Control Tower are removed, including any blueprints\. The account is moved out of any AWS Control Tower OU and into the **Root** area\. The account is no longer part of a registered OU, and it is no longer subject to AWS Control Tower SCPs\. You can close the account through AWS Organizations\.

Unmanaging an account also can be done in the AWS Service Catalog console by an IAM Identity Center user in the **AWSAccountFactory** group, by terminating the Provisioned Product\. For more information on IAM Identity Center users or groups, see [Manage Users and Access Through AWS IAM Identity Center \(successor to AWS Single Sign\-On\)](sso.md)\. The following procedure describes how to unmanage a member account in AWS Service Catalog\.

**To unmanage an enrolled account**

1. Open the AWS Service Catalog console in your web browser at [https://console.aws.amazon.com/servicecatalog](https://console.aws.amazon.com/servicecatalog)\.

1. From the left navigation pane, choose **Provisioned products list**\.

1. From the list of provisioned accounts, choose the name of the account that you want AWS Control Tower no longer to manage\.

1. On the **Provisioned product details** page, from the **Actions** menu, choose **Terminate**\.

1. From the dialog box that appears, choose **Terminate**\.
**Important**  
The word *terminate* is specific to AWS Service Catalog\. When you terminate an Account Factory account in AWS Service Catalog, the account is not closed\. This action removes the account from its OU and your landing zone\.

1.  When the account has been unmanaged, its status changes to **Not Enrolled**\.

1. If you no longer need the account, close it\. For more information about closing AWS accounts, see [Closing an Account](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/close-account.html) in the *AWS Billing User Guide*

When you unmanage a customized account, AWS Control Tower removes the resources that the blueprint has deployed, as well as any other resources that AWS Control Tower created within the account\. After you unmanage the account, you can close the account through AWS Organizations\.

**Note**  
An unmanaged account is not closed or deleted\. When the account has been unmanaged, the IAM Identity Center user that you selected when you created the account in Account Factory still has administrative access to the account\. If you do not want this user to have administrative access, you must change this setting in IAM Identity Center by updating the account in Account Factory and changing the IAM Identity Center user email address for the account\. For more information, see [Update and move account factory accounts with AWS Control Tower or with AWS Service Catalog](updating-account-factory-accounts.md)\.

## Video Walkthrough<a name="unmanage-account-video"></a>

This video \(3:25\) describes how to remove an account from AWS Control Tower, gain root access to the account, and finally close the AWS account\. You also can close an account with [an AWS Organizations API](https://docs.aws.amazon.com/controltower/latest/userguide/delete-account.html)\. For better viewing, select the icon at the lower right corner of the video to enlarge it to full screen\. Captioning is available\.

You can view a list of AWS [YouTube videos](https://www.youtube.com/playlist?list=PLhr1KZpdzukdS9skEXbY0z67F-wrcpbjm) that explain common tasks in AWS Control Tower\.