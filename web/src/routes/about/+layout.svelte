<script lang="ts">
    import { t } from "$lib/i18n/translations";

    import PageNav from "$components/subnav/PageNav.svelte";

    import PageNavTab from "$components/subnav/PageNavTab.svelte";
    import PageNavSection from "$components/subnav/PageNavSection.svelte";

    import IconLock from "@tabler/icons-svelte/IconLock.svelte";
    import IconComet from "@tabler/icons-svelte/IconComet.svelte";
    import IconChecklist from "@tabler/icons-svelte/IconChecklist.svelte";
    import IconUsersGroup from "@tabler/icons-svelte/IconUsersGroup.svelte";
    import IconHeartHandshake from "@tabler/icons-svelte/IconHeartHandshake.svelte";
</script>

<PageNav
    pageName="about"
    homeNavPath="/about"
    homeTitle={$t("tabs.about")}
    contentPadding
    wideContent
>
    <svelte:fragment slot="navigation">
        <PageNavSection>
            <PageNavTab
                path="/about/general"
                title={$t("about.page.general")}
                icon={IconComet}
                iconColor="blue"
            />
            <PageNavTab
                path="/about/community"
                title={$t("about.page.community")}
                icon={IconUsersGroup}
                iconColor="purple"
            />
        </PageNavSection>

        <PageNavSection>
            <PageNavTab
                path="/about/privacy"
                title={$t("about.page.privacy")}
                icon={IconLock}
                iconColor="blue"
            />
            <PageNavTab
                path="/about/terms"
                title={$t("about.page.terms")}
                icon={IconChecklist}
                iconColor="green"
            />
            <PageNavTab
                path="/about/credits"
                title={$t("about.page.credits")}
                icon={IconHeartHandshake}
                iconColor="magenta"
            />
        </PageNavSection>
    </svelte:fragment>

    <slot slot="content"></slot>
</PageNav>
