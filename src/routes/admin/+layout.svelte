<script>
    import { LayoutDashboard, Inbox, Cog, CircleHelp, ChevronLeft } from '@lucide/svelte';
    import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    let { children } = $props();
</script>


<Sidebar class="m-8 mt-24">
    <SidebarWrapper>
        <SidebarGroup>
            <SidebarItem class="flex justify-end">
                <svelte:fragment slot="icon">
                    <ChevronLeft/>
                </svelte:fragment>
            </SidebarItem>
            <SidebarItem label="Dashboard" href="/admin/dashboard">
                <svelte:fragment slot="icon">
                    <LayoutDashboard />
                </svelte:fragment>
            </SidebarItem>
            <SidebarItem label="Inbox" href="/admin/dashboard/inbox">
                <svelte:fragment slot="icon">
                    <Inbox />
                </svelte:fragment>
            </SidebarItem>
            <SidebarGroup border>
                <SidebarItem label="Settings">
                    <svelte:fragment slot="icon">
                        <Cog />
                    </svelte:fragment>
                </SidebarItem>
                <SidebarItem label="Support">
                    <svelte:fragment slot="icon">
                        <CircleHelp />
                    </svelte:fragment>
                </SidebarItem>
            </SidebarGroup>
        </SidebarGroup>
    </SidebarWrapper>
</Sidebar>

<main>
    {@render children()}
</main>


