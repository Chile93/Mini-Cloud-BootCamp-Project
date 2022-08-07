# How to delete the Multiple Cloud Providers resources

**First step - Empty your bucket**

- Access the AWS Console and open S3 Service.
- Select your bucket and click on Empty.
- To confirm deletion, type *permanently delete* in the text input field.
- Click on Empty.

**First step concluded! 🎉**

**Second step - Set the instance deletion_protection from true to false**

- Open the Google Editor, and access the following path: mission1_en/mission1/en/terraform/. Now, open the tcb_gcp_database.tf file
- On line 11 of the tcb_gcp_database.tf file:
    - Replace from deletion_protection = “true” to deletion_protection = “false”
    **Example:**
        - First version: deletion_protection = "true”
        - Updated version: deletion_protection = "false”
        
- Change from Editor to Terminal
- Run the commands to apply the terraform file changes:

```
cd ~/mission1_en/mission1/en/terraform/

terraform apply
	***Enter a value: yes***
```

Now, you’re ready to delete all the resources with the terraform destroy. 🚀

- Run the following command:

```
terraform destroy
	***Enter a value: yes***
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fafc4631-04ca-4431-a5c4-3950d8bd24ad/Untitled.png)

**Congratulations! All resources were deleted from multiple Cloud Providers with just a command!**
