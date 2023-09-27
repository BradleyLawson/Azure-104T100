# Verify Custom Domain Names

When an administrator adds a custom domain name to an Azure Active Directory (Azure AD) instance, the custom domain name is initially in an unverified state. Azure AD does not allow any directory resources to use an unverified custom domain name.

Before you can use a custom domain name for your Azure AD instance, you must verify ownership of your custom domain name.

## How to Verify Your Custom Domain Name

After you've added a custom domain name for your Azure AD instance in the Azure portal, you need to initiate the verification process to confirm ownership of your custom domain name.

The verification process involves adding a DNS record for your custom domain name. The DNS record can be of type MX (Mail exchange) or TXT (Text). Here's how to do it:

1. Access the Azure portal.

2. Navigate to the DNS settings for your custom domain name.

3. Add the DNS record to your custom domain name. You can choose either an MX record or a TXT record.

   - The MX record lists mail exchange servers that accept email for your domain.
   - The TXT record contains human-readable or machine-readable data about your domain. These record types are defined in RFC 1035.

4. Save the DNS record settings.

   **Note:** The Azure verification process may take several minutes or even hours to complete.

Once Azure verifies the presence of the DNS record for your custom domain name, it will add your new custom domain name to your Azure AD instance subscription. This verified custom domain name can then be used within your Azure AD instance for various purposes.
