# Assignment-5-vp
﻿
Microsoft Visual Studio Solution File, Format Version 12.00
# Visual Studio Version 17
VisualStudioVersion = 17.2.32505.173
MinimumVisualStudioVersion = 10.0.40219.1
Project("{FAE04EC0-301F-11D3-BF4B-00C04F79EFBC}") = "CityRepository", "CityRepository\CityRepository.csproj", "{C9825688-5A3E-4E18-AB8C-68540D3A3102}"
EndProject
Global
	GlobalSection(SolutionConfigurationPlatforms) = preSolution
		Debug|Any CPU = Debug|Any CPU
		Release|Any CPU = Release|Any CPU
	EndGlobalSection
	GlobalSection(ProjectConfigurationPlatforms) = postSolution
		{C9825688-5A3E-4E18-AB8C-68540D3A3102}.Debug|Any CPU.ActiveCfg = Debug|Any CPU
		{C9825688-5A3E-4E18-AB8C-68540D3A3102}.Debug|Any CPU.Build.0 = Debug|Any CPU
		{C9825688-5A3E-4E18-AB8C-68540D3A3102}.Release|Any CPU.ActiveCfg = Release|Any CPU
		{C9825688-5A3E-4E18-AB8C-68540D3A3102}.Release|Any CPU.Build.0 = Release|Any CPU
	EndGlobalSection
	GlobalSection(SolutionProperties) = preSolution
		HideSolutionNode = FALSE
	EndGlobalSection
	GlobalSection(ExtensibilityGlobals) = postSolution
		SolutionGuid = {1FDF0183-1933-4FC8-88ED-A80E31E5BF57}
	EndGlobalSection
EndGlobal


@page "/citybuttons"
@using YourNamespace // Replace with the namespace of CityRepository
@inject NavigationManager Navigation

<h3>Cities</h3>

<!-- City Buttons -->
<div>
    @foreach (var city in CityRepository.GetCities())
    {
        <button class="btn btn-primary m-1" @onclick="() => NavigateToCity(city)">
            @city
        </button>
    }
</div>

<hr />

<!-- Placeholder for Server List -->
<h3>Server List</h3>
<p>The server list content will be displayed here.</p>

@code {
    /// <summary>
    /// Navigates to a city-specific route or handles city button click.
    /// </summary>
    /// <param name="city">Name of the city clicked.</param>
    private void NavigateToCity(string city)
    {
        // Example: Navigate to a route associated with the city (if applicable)
        Navigation.NavigateTo($"/city/{city}");
    }
}




