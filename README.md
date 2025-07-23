# AWS Simple Storage Service (S3)
Step-by-step process** for your AWS S3 Mini Project based on the description and learning goals:
## Phase 1: Preparation & Prerequisites
### Step 1: Set Up Your AWS Free Tier Account
If not done already:
* Go to [https://aws.amazon.com/free](https://aws.amazon.com/free)
* Create an account
* Set up billing alerts to avoid unexpected charges
#
## Phase 3: Hands-On Implementation
### Step 4: Create an S3 Bucket
1. Log in to AWS Console
2. Navigate to “S3” under “Storage”
3. Click “Create bucket”
4. Configure:
   * Bucket name (must be globally unique)
   * AWS region
   * Disable/Enable public access (keep public access blocked for private use)
   * Leave versioning disabled for now (we’ll enable it later)
   * Click “Create Bucket”
#
### Step 5: Upload Files to the Bucket
1. Click on the bucket name
2. Click “Upload”
3. Add files or folders from your computer
4. Leave default storage class and permissions for now
5. Click “Upload”
#
### Step 6: Enable Versioning on the Bucket

1. Navigate to the bucket's “Properties” tab
2. Scroll to “Bucket Versioning”
3. Click “Edit” → “Enable” → Save changes
4. Re-upload a file with the same name to observe version tracking
5. Review versions under the “Versions” tab in the bucket
#
### Step 7: Configure Permissions for Objects
1. Go to the “Permissions” tab of the bucket
2. Adjust:
   * “Bucket Policy”: Write a custom JSON policy if needed
   * “Access Control List (ACL)”: Add specific users or allow public access
3. Try making a file public (for demo purposes):
   * Select the object → “Actions” → “Make public using ACL”
#
### Step 8: Implement Lifecycle Policy
1. Go to the “Management” tab of the bucket
2. Click “Create lifecycle rule”
3. Name your rule (e.g., "Archive old files")
4. Add transitions:
   * Move objects to “Glacier” after 30 days
   * Delete objects after 365 days
5. Save the rule
#
## Phase 4: Wrap-Up and Review
### Step 9: Clean Up Resources
* Delete unnecessary objects
* Remove lifecycle rules (if any)
* Delete the bucket to avoid charges:

  * Empty the bucket first
  * Go back to S3 dashboard → Select bucket → “Delete”
#
### Step 10: Reflect on Learning Outcomes
Ensure you can:
* Create and configure buckets
* Upload and manage files
* Understand how versioning protects against overwrites
* Control access using permissions
* Automate storage management with lifecycle rules
#
## Optional Extensions
* Use the AWS CLI to perform S3 operations (e.g., `aws s3 ls`, `aws s3 cp`)
* Explore “static website hosting” with S3
* Set up “logging and monitoring” with CloudWatch
