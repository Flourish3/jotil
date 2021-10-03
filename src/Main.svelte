<script lang="ts">
    import Contact, { ContactInfo } from "./Contact.svelte";

    let contactList: ContactInfo[] = [
        {
            link: "mailto:johan.tillmar@protonmail.com",
            name: "Mail",
            iconLink: "email.svg"
        },
        {
            link: "https://se.linkedin.com/in/johan-tillmar-b7122799",
            name: "LinkedIn",
            iconLink: "linkedin.svg"
        }
    ];
</script>

<main>
    <h1>Jotil Konsult</h1>
    <p>Bedriver konsultverksamhet inom IT</p>
    <Contact  contactInfo={contactList}/>
</main>

<style>
	main {
        display: grid;
        grid-template-rows: 1fr 1fr auto;
		text-align: center;
		padding: 0.5em;
        background-color: rgb(205, 225, 226);
        height: 98vh;
        border-radius: 15px;
	}

	h1 {
		color: rgb(36, 37, 49);
		font-size: 4.5em;
		font-weight: 1;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
