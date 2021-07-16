# **FreeAgent Applet Library**
Use this library to sync and connect with FreeAgent Applets

### Start using it with
    import { FAAppletClient } from '@freeagentsoftwareinc/freeagent-applet-library/promise';

	const FAClient = new FAAppletClient({
	    appletId: YOUR_APPLET_ID,
    });
    
![enter image description here](https://i.imgur.com/KRTC2Zc.png)
*You can find it under App Configuration > APPLET CONFIGURATION*

### Queries

    const values = await FAClient.listEntityValues({
	    entity: String!,
	    fields: [String],
	    id: String,
	    order: [[String]],
	    limit: Int,
	    offset: Int,
	    aggType: String,
	    aggField: String,
	    pattern: String,
	    filters: [Filter],
	    userTimezone: String,
	    parent_entity_reference_id: String,
	    fields_from_card_layout: Boolean,
	    show_hidden: Boolean,
	    included_lines: [String],
	    include_all_lines: Boolean,
	    from_settings_view: Boolean
    });

### Mutations

    const upsertedRecord = await FAClient.upsertCompositeEntity({
	    id: '31d9ca46-83da-45af-a3e8-dc4703bfc91f',
	    entity: "test_w_line",
	    m2m_custom_field: null,
	    m2m_instance_id: null,
	    field_values: {
		    description: "Test with line updated from applet",
		},
	    children: [{
		    entity:  "test_line",
	        field_values: {
		        description:  "Test line",
	        },
        }],
	});
