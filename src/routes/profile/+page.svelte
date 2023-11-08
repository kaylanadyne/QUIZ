<script>
    import Navbar from "/src/components/Navbar.svelte";
    let showBeranda = false;
    let showRiwayat = false;
    import ProfileTab from "/src/components/ProfileTab.svelte";
    import SettingTab from "/src/components/SettingTab.svelte";
    import Tabs from "/src/components/Tabs.svelte";

  let items = [
    { label: "Akun",
		 value: 1,
		 component: ProfileTab
		},
    { label: "Pengaturan",
		 value: 2,
		 component: SettingTab
		}
  ];
</script>
<Navbar {showBeranda} {showRiwayat} />
<Tabs {items} />