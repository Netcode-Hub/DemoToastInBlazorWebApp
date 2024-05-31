# Toast of the Town : Effortlessly Implementing Toast Notifications in Your  .NET 8 Web Applications https://youtu.be/j7_AgPgmhAo
![Toast Server](https://github.com/Netcode-Hub/DemoToastInBlazorWebApp/assets/110794348/6842c1da-97a3-419b-8d4c-03408bc62ecc)

# How to use version 1.0.0
# Install the package 
      *NetcodeHub.Packages.Components.Toast *

# Register Toast Service in the Program.cs file**
        *builder.Service.AddScope<ToastService>();*

# Add Namespace
    *@using NetcodeHub.Packages.Components.Toast*

# Inject Toast Service
       *@inject ToastService ToastService*
     *<Toast @ref="toastService.ToastComponent" IconClass="bi bi-check" Persist="false"/>*
       *<button class="btn btn-info" @onclick="ShowToast">Show Toast</button>*
<br />

@code{

             void ShowToast() =>toastService.ShowDangerToast("Title", "Message");
             void ShowToast() =>toastService.ShowInfoToast("Title", "Message");
             void ShowToast() =>toastService.ShowSuccessToast("Title", "Message");
             void ShowToast() =>toastService.ShowWarningToast("Title", "Message");

}


# How to use version 1.0.4
# What is New?
1. Introduction of Toast Position.
     a. Top
     b. Bottom
# What is changed from version 1.0.0?
1. No more injection of ToastService making it easy to use.
   Follw the below guidelines and choose version of choice.
   
# Install the package 
                  NetcodeHub.Packages.Components.Toast


# Add package Namespace to the _Import.razor file
               @using static NetcodeHub.Packages.Components.Toast.NetcodeHubToast

# Use the package
                 <NetcodeHubToast @ref="ToastComponent" 
                                  Position="@ToastPosition.Bottom / Top" 
                                  IconClass="bi bi-check" 
                                  Persist="false" 
                                  Duration=4000/>

                   <button class="btn btn-info" @onclick="ShowToast">Show Toast</button>
            <br />

            @code{
                    NetcodeHubToast? ToastComponent;

                    async Task ShowToast() => 
                                await ToastComponent!.ShowDangerToast("Title", "Message");

                    async Task ShowToast() =>
                                await ToastComponent!.ShowInfoToast("Title", "Message");

                    async Task ShowToast() =>
                                await ToastComponent!.ShowSuccessToast("Title", "Message");

                    async Task ShowToast() =>
                                await ToastComponent!.ShowWarningToast("Title", "Message");

                }



/*Follow Netcode-Hub*/ <br/>
https://netcodehub.blogspot.com <br/> 
https://github.com/Netcode-Hub <br/>
https://twitter.com/NetcodeHub | Twitter <br/>
https://web.facebook.com/NetcodeHub | Facebook <br/>
https://www.linkedin.com/in/netcode-hub-90b188258/ | LinkedIn <br/>

/*You can buy a coffee for me to support the channel*/ ☕️ <br/>
https://www.buymeacoffee.com/NetcodeHub <br/>
<a href="https://www.buymeacoffee.com/NetcodeHub" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a> <br/>
PLEASE DO NOT FOGET TO STAR THIS REPOSITORY<br/>
