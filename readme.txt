=== Cart2Cart: Magento to WooCommerce Migration   ===
Contributors: cart2cart
Tags: magento to woocommerce, magento to woocommerce migration, migrate magento to woocommerce
Requires at least: 3.8.1
Tested up to: 3.8.1
Stable tag: 3.8.1
License: GPLv2
License URI: http://www.gnu.org/licenses/gpl-2.0.html 
Plugin helps to migrate all data from Magento to WooCommerce automatically with no programming skills required.

== Description ==
The plugin will help you to migrate all your data from Magento to WooCommerce automatically. You will be able to transfer products, customers, orders with all corresponding information accurately and effortlessly. 

= The following entities can be moved from Magento to WooCommerce:
 =
* Products, product images, product extra fields, product attributes, product variants
* Categories, category images 
* Customers, customer shipping address, customer billing address 
* Orders, order statuses

*Supported Magento versions:*  1.1.x - 1.8.x CE, 1.6.x-1.13.x EE
*Supported WooCommerce versions:* 1.4.x, 1.5.x, 1.6.x, 2.0.x (new software versions are constantly being added).

= Features of Automated Migration with Cart2Cart:
 =
- **Simple** - no programming skills required, simply follow a step by step instruction.
- **Fast** - the time of migration depends on a quantity of entities you wish to move and takes a few hours. 
- **Free Demo** - up to 10 entities will be moved for free
- **Support** - contact support team via live chat, phone or ticket at any convenient time.

**Note.** *Plugin supports entities migration only, Magento theme won’t be converted into WooCommerce theme.This plugin installs connection bridges at your Magento and WooCommerce, which is needed for data interaction between two platforms. Upon activation, you’ll be redirected to Cart2Cart website in order to launch the conversion.*

= Steps to Take before Migration =
1. Install WooCommerce and make sure that Magento and WooCommerce stores are available online.
1. Have Magento store FTP access details at hand (host, username, password) - you use them to install connection bridge on Magento.

 

== Installation ==

1. Download the plugin zip file
1. Extract plugin zip file to your PC
1. Upload extracted file to wp-content/plugin directory
1. Go to Admin -> Go to Admin -> Plugins, find “Cart2Cart Magento to WooCommerce Migration” and click Activate
1. You’ll be redirected to Cart2Cartwebsite in order to complete your migration

== Frequently Asked Questions ==
= Are there any technical requirements for migration performance? =
There are no universal technical requirements for all stores as different platforms have different technical peculiarities. However, there are some recommendation you should consider before setting shopping cart migration.
Recommended PHP configurations:
memory_limit - 128M (512M for Magento)<br>
post_max_size - 16M<br>
max_execution_time - 60<br>
If Suhosin module is installed:<br>
suhosin.post.max_value_length - 16777216<br>
suhosin.request.max_value_length - 16777216<br>
Also, it is recommended to switch off the limits for the number of requests to server, as well as firewalls and basic authentication.


= Can I be sure of data security Cart2Cart? =Cart2Cart performs migration using a separate Amazon EC2 server and all data is deleted after the process has been finished.
Cart2Cart does not migrate client’s credit card information and passwords.
We use secure HTTPS protocol for all connections and only authorized staff has access to the migration process.
= How can I enable Custom fields in WooCommerce? =
Cart2Cart supports migration of Custom fields to WooCommerce 2.x. However, WooCommerce doesn’t display Custom fields by default.
To enable this option you have to:<br>
go to "store/wp-content/plugins/woocommerce/templates/single-product/tabs"<br>
find file "additional-information.php"<br>
add the following code: echo '<table class="shop_attributes"><tbody>'; foreach(get_post_meta($post->ID, $key, true) as $key => $attr) { if(strpos($key, "_") !== 0) { echo '<th>'.$key.'</th>'; echo '<td>'.array_shift($attr).'</td>'; echo '</tr>'; } }	 echo '</tbody></table>';


= Is there a possibility to migrate reviews to WooCommerce? =
Yes, Cart2Cart supports migration of reviews while moving to WooCommerce. Moreover, review ratings will be moved together with reviews.

= WooCommerce multiple languages migration ="No other languages apart from English were migrated to WooCommerce. The products/orders/customers in other languages do not show." It is due to the technical characteristics of the platform that multiple languages are not migrated. WooCommerce doesn't support multi-languages by default. So, Cart2Cart migrates only one default language.

= Invalid response received =
Сontact us at support@shopping-cart-migration.com

= An error occurred when trying to connect to your site =
Сontact us at support@shopping-cart-migration.com

= An unknown error occurred =
Сontact us at support@shopping-cart-migration.com

== Screenshots ==

1. /assets/screenshot-1.jpg
2. /assets/screenshot-2.jpg 
3. /assets/screenshot-3.jpg
4. /assets/screenshot-4.jpg
5. /assets/screenshot-5.jpg

== Changelog ==

= 1.0 =* Initial commit