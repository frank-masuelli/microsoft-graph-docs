---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Bookings

$params = @{
	"@odata.type" = "#microsoft.graph.bookingAppointment"
	CustomerTimeZone = "America/Chicago"
	SmsNotificationsEnabled = $true
	EndDateTime = @{
		"@odata.type" = "#microsoft.graph.dateTimeTimeZone"
		DateTime = "2018-05-01T12:30:00.0000000+00:00"
		TimeZone = "UTC"
	}
	IsLocationOnline = $true
	OptOutOfCustomerEmail = $false
	PostBuffer = "PT10M"
	PreBuffer = "PT5M"
	Price = 10
	"PriceType@odata.type" = "#microsoft.graph.bookingPriceType"
	PriceType = "fixedPrice"
	"Reminders@odata.type" = "#Collection(microsoft.graph.bookingReminder)"
	Reminders = @(
		@{
			"@odata.type" = "#microsoft.graph.bookingReminder"
			Message = "This service is tomorrow"
			Offset = "P1D"
			"Recipients@odata.type" = "#microsoft.graph.bookingReminderRecipients"
			Recipients = "allAttendees"
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingReminder"
			Message = "Please be available to enjoy your lunch service."
			Offset = "PT1H"
			"Recipients@odata.type" = "#microsoft.graph.bookingReminderRecipients"
			Recipients = "customer"
		}
		@{
			"@odata.type" = "#microsoft.graph.bookingReminder"
			Message = "Please check traffic for next cater."
			Offset = "PT2H"
			"Recipients@odata.type" = "#microsoft.graph.bookingReminderRecipients"
			Recipients = "staff"
		}
	)
	ServiceId = "57da6774-a087-4d69-b0e6-6fb82c339976"
	ServiceLocation = @{
		"@odata.type" = "#microsoft.graph.location"
		Address = @{
			"@odata.type" = "#microsoft.graph.physicalAddress"
			City = "Buffalo"
			CountryOrRegion = "USA"
			PostalCode = "98052"
			PostOfficeBox = $null
			State = "NY"
			Street = "123 First Avenue"
			"Type@odata.type" = "#microsoft.graph.physicalAddressType"
			Type = $null
		}
		Coordinates = $null
		DisplayName = "Customer location"
		LocationEmailAddress = $null
		"LocationType@odata.type" = "#microsoft.graph.locationType"
		LocationType = $null
		LocationUri = $null
		UniqueId = $null
		"UniqueIdType@odata.type" = "#microsoft.graph.locationUniqueIdType"
		UniqueIdType = $null
	}
	ServiceName = "Catered bento"
	ServiceNotes = "Customer requires punctual service."
	StartDateTime = @{
		"@odata.type" = "#microsoft.graph.dateTimeTimeZone"
		DateTime = "2018-05-01T12:00:00.0000000+00:00"
		TimeZone = "UTC"
	}
	MaximumAttendeesCount = 5
	FilledAttendeesCount = 1
	"Customers@odata.type" = "#Collection(microsoft.graph.bookingCustomerInformation)"
	Customers = @(
		@{
			"@odata.type" = "#microsoft.graph.bookingCustomerInformation"
			CustomerId = "7ed53fa5-9ef2-4f2f-975b-27447440bc09"
			Name = "Jordan Miller"
			EmailAddress = "jordanm@contoso.com"
			Phone = "213-555-0199"
			Notes = $null
			Location = @{
				"@odata.type" = "#microsoft.graph.location"
				DisplayName = "Customer"
				LocationEmailAddress = $null
				LocationUri = ""
				LocationType = $null
				UniqueId = $null
				UniqueIdType = $null
				Address = @{
					"@odata.type" = "#microsoft.graph.physicalAddress"
					Street = ""
					City = ""
					State = ""
					CountryOrRegion = ""
					PostalCode = ""
				}
			}
			TimeZone = "America/Chicago"
			CustomQuestionAnswers = @(
			)
		}
	)
}

New-MgBookingBusinessAppointment -BookingBusinessId $bookingBusinessId -BodyParameter $params

```