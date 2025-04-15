Charge people to keep their data and deliver to posterity years down the line (set conditions)
	Horizontally integrate hosting providers to be able to immortalize websites and social media profiles as well
	Horizontally integrate data collection services to store your digital footprint in its entirety, potentially also deleteMe partnership to get removed from the people you don't want to have them (if already doing search, can outsource search to them and let them advertize ability to delete it all everywhere but on your backups)
Re-inventing RAID in a world where people want to be remembered easier.
Was thinking about how backups work; thought up new (p sure its just raid) system:

### Drives:
1. Working drive (plugged into your computer for use)
2. Daily Backup drive
	Can be cloud
3. Formattable drive for testing of backups
	Can test:
		File integrity
		Physical Device health
			Speed
4. Main backup drive
		Scale to size needed, can even keep copies of old backups for history (and in case you delete something you shouldn't've)
		Can use git to save storage
			Only keep how the files changed and have some way to restore the drive at any period of time to not keep full backups and duplicate storage unnecessarily.
			Set up drive index backup (hashes)
			Use to read 
5. Backup Drive 


---

## Commercialization nuances
### Cybersecurity (The data bank)
If the drives are sold as one unit and controlled by software that means they are at risk of being hacked and losing all of their data

While having your daily backup drive be something cloud based can allow for some separation; if passwords have been compromised then there's no way of keeping your data truly safe without physical separation and more. 

One probable solution is to have the company take backups as well, and/or use an AI for screening the changelogs between backups to ensure no malicious changes have occurred (AI for flag on top of algorithm for flag; both alert manual review to train the AI more) 
	WE HAVE NO WRITE PERMISSIONS ON THEIR DATA, in the event of a hack on our end nothing can affect their backups
		Go as far to send them notifications that we are under attack and to protect their backups (which would require attackers to coordinate enough to take out both backups; could be upgraded to have copies of your data at multiple facilities for a premium)
	Possibly encrypt their data so nothing can execute; def needs to be lossless

Each facility needs to have three chambers; three replicates of the data. In the event of failure the risk of knocking out both 

Discount for allowing ai to train on it
	And credits for if it is utilized in an actual model (aka incentivizing the curation of better content)
		Potentially serve as data marketplace, sell rights to train on data
		Researchers can actually get compensated for their work now
			Can potentially use facilities to get copy of annas archive / libgen / scihub
				Train better AI with better data


With our backups, provide security feed for users of the vault their data is in
