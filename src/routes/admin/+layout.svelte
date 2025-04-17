<script>
    import { LayoutDashboard, Inbox, Cog, CircleHelp, ChevronLeft, ChevronDown, MessagesSquare } from '@lucide/svelte';
    import { Sidebar, SidebarDropdownItem, SidebarDropdownWrapper, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    let { children } = $props();
</script>


<div class="flex">
    <!-- Fixed sidebar that takes full height -->
    <div class="sticky top-0 left-0 z-10 h-full w-72 pt-24 px-8">
        <Sidebar class="h-[calc(100dvh-6rem)]">
            <SidebarWrapper>
                <SidebarGroup>
                    <SidebarItem>
                        <svelte:fragment slot="icon">
                            <ChevronLeft/>
                        </svelte:fragment>
                    </SidebarItem>
                    <SidebarItem label="Dashboard" href="/admin/dashboard">
                        <svelte:fragment slot="icon">
                            <LayoutDashboard />
                        </svelte:fragment>
                    </SidebarItem>
                    <SidebarDropdownWrapper label="Feedback">
                        <svelte:fragment slot="icon">
                            <MessagesSquare />
                        </svelte:fragment>
                        <SidebarDropdownItem label="Inbox">
                            <svelte:fragment slot="icon">
                                <ChevronDown />
                            </svelte:fragment>
                        </SidebarDropdownItem>
                    </SidebarDropdownWrapper>
                    <SidebarItem label="Inbox" href="/admin/dashboard/inbox">
                        <svelte:fragment slot="icon">
                            <Inbox />
                        </svelte:fragment>
                    </SidebarItem>
                    <SidebarGroup border>
                        <SidebarItem label="Settings" href="/admin/dashboard/settings">
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
    </div>

    <main class="flex-1 pt-24 px-8 w-full">
        {@render children()}
    </main>

</div>